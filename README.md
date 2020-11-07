# TcpServerKit

TcpServerKit Unity client implement

```javascript
Import `TcpServerKit_UnityClient.unitypackage`

Add `MuClient.prefab` from TcpClientKit folder


Add a new script with a field of type `ClientListener`

```javascript
[SerializeField] private ClientListener listener;
```
Add required namespace

```javascript
using TcpClientKit;
using static TcpClientKit.Client;
```

Set connection event.
Client.ConnectResult += (ConnectingStatus cs) =>
{
};
```

Add listeners
```javascript
Client.On("Login", LoginResult);
```

Start client
```javascript
listener.Init();
Client.InitServer();
```

For reconnecting
```javascript
Client.CloseConnection();
listener.Init();
Client.InitServer();
```
