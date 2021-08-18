# Python Console

- [Python Net](https://pythonnet.github.io/)
- [Package Link](https://docs.uklnity3d.com/Packages/com.unity.scripting.python@4.0/manual/PythonScriptEditor.html)

## Manifest 

```json
"com.unity.scripting.python": "4.0.0-exp.5"
```

## Notes

I really like PySide example.
I would like to create something using that technology.

### Pip installment

`Library/PythonInstall/Lib/site-packages` - installation location

```powershell
pip install PySide2

pip freeze > ProjectSettings/requirements.txt
```


### Run from CSharp

```CSharp
using UnityEditor.Scripting.Python;
using UnityEditor;

public class HelloWorld
{
    [MenuItem("Python/Hello World")]
    static void PrintHelloWorldFromPython()
    {
        PythonRunner.RunString(@"
                import UnityEngine;
                UnityEngine.Debug.Log('hello world')
                ");
    }
}
```

### Low Level API

```CSharp
using Python.Runtime;
using UnityEditor.Scripting.Python;

public class MyPythonScript
{
    [MenuItem("MyPythonScript/Run")]
    public static void Run()
    {
        PythonRunner.EnsureInitialized();
        using (Py.GIL()) {
            try {
                dynamic sys = PythonEngine.ImportModule("sys");
                UnityEngine.Debug.Log($"python version: {sys.version}");
            } catch(PythonException e) {
                UnityEngine.Debug.LogException(e);
            }
        }
    }
}
```

### Python example

```Python
import UnityEngine

all_objects = UnityEngine.Object.FindObjectsOfType(UnityEngine.GameObject)
for go in all_objects:
    if go.name[-1] != '_':
        go.name = go.name + '_'
```

