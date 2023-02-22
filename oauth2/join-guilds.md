---
description: This requires the Access Token and the Token for the bot
---

# Join Guilds

This uses the "guilds.join" scope but remember that the bot also needs to be in the server with "Create Instant Invite" permission!

```javascript
OAuth2.joinServer(guild_id, user_id, access_token).then((x) => {
    console.log(x)
}).catch((x) => {
    console.log(x)
})
```

If you receive nothing it means success if you get something like bellow its also success else it failed.

```json
{
  "avatar": null,
  "communication_disabled_until": null,
  "flags": 1,
  "is_pending": false,
  "joined_at": '...',
  "nick": null,
  "pending": false,
  "premium_since": null,
  "roles": [],
  "user": {
    "id": '...',
    "username": '...',
    "display_name": null,
    "avatar": '...',
    "avatar_decoration": null,
    "discriminator": '....',
    "public_flags": 0
  },
  "mute": false,
  "deaf": false
}
```
