## Photon

## Outline
    1. PhotonEngine
    2. MonoBehaviourPUN
    3. PhotonView
    5. IPunCallback
    4. IPunObserbable
    6. RaiseEvent
    7. NetworkManager
    8. RoomProperties


<h3 style=color:gray><a>static</a> <a >class </a> PhotonEngine {}</h3>

>Main **static** - *toolkit for interaction with Photon Network*
```csharp

PhotonEngine.Connect();
PhotonEngine.JoinLobby();

PhotonEngine.EnterRoom();
PhotonEngine.ExitRoom();

PhotonEngine.RPC("name",BufferType.AllBuffer)

PhotonEngine.LoadLevel();
- PhotonEngine.OfflineMode();
```

<h3 style=color:gray><a>class</a>  MonoBehaviourPun </h3>

>MonoBehaviour from **PUN** - *easy ref to photonView*
```csharp
private PhotoneView photonView;
```

<h3 style=color:gray;><a>class</a> <a style=color:black>PhotonView</a> : MonoBehaviour </h3>

>MonoBehaviour from **PUN** - *easy ref to photonView*
```csharp
public bool IsMine{get;} // Is local instance
public int  Id{get;} // Is local instance
- public IPunObservable[] watched;
[RPC]
public void Some(); // new command that will be executed;

```
