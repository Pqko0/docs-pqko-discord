---
description: This requires Access Token
---

# Get Guilds

This requires the "guilds" scope.

```javascript
OAuth2.getServers(access_token).then((x) => {
    console.log(x)
}).catch((x) => {
    console.log(x)
})
```

You will receive a array of servers from the user saying if they are owner, features, permissions and other stuff!

```json
[{
    "id": "...",
    "name": "...",
    "icon": null,
    "owner": true,
    "permissions": 0,
    "features": ["APPLICATION_COMMAND_PERMISSIONS_V2"],
    "permissions_new": "..."
}, {
    "id": "...",
    "name": "...",
    "icon": null,
    "owner": false,
    "permissions": 0,
    "features": ["APPLICATION_COMMAND_PERMISSIONS_V2"],
    "permissions_new": "..."
}, {
    "id": "...",
    "name": "...",
    "icon": null,
    "owner": true,
    "permissions": 0,
    "features": ["APPLICATION_COMMAND_PERMISSIONS_V2"],
    "permissions_new": "..."
}, {
    "id": "...",
    "name": "...",
    "icon": null,
    "owner": false,
    "permissions": 0,
    "features": ["APPLICATION_COMMAND_PERMISSIONS_V2"],
    "permissions_new": "..."
}]
```
