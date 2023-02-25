---
description: Returns guild channels
---

# Get Guild Channels

Must be in server and also returns channels it can see (I think)

```javascript
oauth.getGuildChannels(guildID).then((x) => console.log(x))
```

And here is the return

```json
[
  {
    id: '1079088371017728082',
    type: 4,
    name: 'Text Channels',
    position: 0,
    flags: 0,
    parent_id: null,
    guild_id: '1079088370497630258',
    permission_overwrites: []
  },
  {
    id: '1079088371017728083',
    type: 4,
    name: 'Voice Channels',
    position: 0,
    flags: 0,
    parent_id: null,
    guild_id: '1079088370497630258',
    permission_overwrites: []
  },
  {
    id: '1079088371017728084',
    last_message_id: null,
    type: 0,
    name: 'general',
    position: 0,
    flags: 0,
    parent_id: '1079088371017728082',
    topic: null,
    guild_id: '1079088370497630258',
    permission_overwrites: [],
    rate_limit_per_user: 0,
    nsfw: false
  },
  {
    id: '1079088371017728085',
    last_message_id: null,
    type: 2,
    name: 'General',
    position: 0,
    flags: 0,
    parent_id: '1079088371017728083',
    topic: null,
    bitrate: 64000,
    user_limit: 0,
    rtc_region: null,
    guild_id: '1079088370497630258',
    permission_overwrites: [],
    rate_limit_per_user: 0,
    nsfw: false
  }
]
```
