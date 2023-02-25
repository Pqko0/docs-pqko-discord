---
description: This requires the Access Token
---

# Get User Connections

This requires the "connections" scope.

```javascript
OAuth2.getUserConnections(access_token).then((x) => {
    console.log(x)
}).catch((x) => {
    console.log(x)
})
```

This is the response you should receive

```json
{
    "id": "...",
    "name": "...",
    "type": "...",
    "revoked": false,
    "integrations": ["..."],
    "verified": false,
    "friend_sync": false,
    "show_activity": false,
    "visibility": false
}
```
