# Web

## Interacting with Unity from JS
```JavaScript
unityInstance.SendMessage('MyGameObject', 'MyFunction');
unityInstance.SendMessage('MyGameObject', 'MyFunction', 5);

unityInstance.SendMessage('WebAPI   ', 'MyFunction', 'MyString');
```