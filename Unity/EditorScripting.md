# Editor scripting

## ExecuteInEditMode

```csharp
[ExecuteInEditMode]
public class LookAtPoint : MonoBehaviour
{
    public Vector3 lookAtPoint = Vector3.zero;

    void Update()
    {
        transform.LookAt(lookAtPoint);
    }
}
```

##  Custom Editor

```csharp
[CustomEditor(typeof(LookAtPoint))]
[CanEditMultipleObjects]
public class LookAtPointEditor : Editor
{
    SerializedProperty lookAtPoint;

    void OnEnable()
    {
        lookAtPoint = serializedObject.FindProperty("lookAtPoint");
    }

    public override void OnInspectorGUI()
    {
        serializedObject.Update();
        EditorGUILayout.PropertyField(lookAtPoint);
        if (lookAtPoint.vector3Value.y > (target as LookAtPoint).transform.position.y)
        {
            EditorGUILayout.LabelField("(Above this object)");
        }
        if (lookAtPoint.vector3Value.y < (target as LookAtPoint).transform.position.y)
        {
            EditorGUILayout.LabelField("(Below this object)");
        }
        
            
        serializedObject.ApplyModifiedProperties();
    }
}
```
## Custom RenderPiepline Asset

Another thing that I like in this example is it can work with or without editor

```csharp

[ExecuteInEditMode]
public class BasicAssetPipe:RenderPipelineAsset 
{
    [SerializeField]
    private Color _clearColor = Color.green;
#if UNITY_EDITOR
    [UnityEditor.MenuItem("SRPDemo/CreateBasic")]
    static void CreateBasicAssetPipeline()
    {
	var instance = ScriptableObject.CreateInstance<BasicAssetPipe>();
	UnityEditor.AssetDatabase.CreateAsset(instance,"Assets/BleedingPipe.asset");


    }
#endif
```
