# TcpServerKit_Unity

**TcpServerKit Unity client implement**

**get server package https://github.com/mul83rry/TcpServerKit**

import TcpServerKit_UnityCLient.unitypackage


```javascript
Import `TcpServerKit_UnityClient.unitypackage`
```
Drag `MuClient.prefab` from TcpClientKit folder to hierarchy
and set ip and port


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
```javascript
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



*server package*
https://www.nuget.org/packages/TcpServerKit
