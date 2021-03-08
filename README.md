
# TcpServerKit_Unity

**TcpServerKit Unity client implement**

**get server package https://github.com/mul83rry/TcpServerKit**

import TcpServerKit_UnityCLient.unitypackage


```javascript
Import `TcpServerKit_UnityClient.unitypackage`
```
Drag `MuClient.prefab` from TcpClientKit folder to hierarchy
and set ip and port

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

Add listeners (if exists will be replaced)
```javascript
Client.On("Login", LoginResult);
```

Start client
```javascript
Client.InitServer(); or InitServer(Encoding type);
```

For reconnecting
```javascript
Client.CloseConnection();
Client.InitServer(); or InitServer(Encoding type);
```



*server package*
https://www.nuget.org/packages/TcpServerKit
