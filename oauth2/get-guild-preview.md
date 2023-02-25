---
description: Gets guild preview.
---

# Get Guild Preview

Bot must be in server to use

```javascript
oauth.getGuildPreview(guildID).then((x) => console.log(x))
```

And you should get something like this

```json
{
  id: '...',
  name: '...',
  icon: null,
  description: null,
  home_header: null,
  splash: null,
  discovery_splash: null,
  features: [ '...' ],
  approximate_member_count: 1,
  approximate_presence_count: 1,
  emojis: [],
  stickers: []
}
```
