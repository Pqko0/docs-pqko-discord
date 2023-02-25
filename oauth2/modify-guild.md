---
description: Modifies guild via OAuth2
---

# Modify Guild

The JSON parameters are found at : [https://discord.com/developers/docs/resources/guild#modify-guild](https://discord.com/developers/docs/resources/guild#modify-guild)

```javascript
oauth.modifyGuild(guildID, {
    name: "This has been edited!"
}).then((x) => console.log(x))
```

Returns the new editied/modified guild as JSON!
