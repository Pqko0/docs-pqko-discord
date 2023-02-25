---
description: >-
  Gets guild information via OAuth2 (Guild ID Required and bot must be in
  server)
---

# Get Guild

Code example

```javascript
oauth.getGuild(guildID).then((x) => console.log(x))
```

The bot currently has admin and gives back this

```json
{
  id: '...',
  name: '...',
  icon: null,
  description: null,
  home_header: null,
  splash: null,
  discovery_splash: null,
  features: [ ... ],
  emojis: [],
  stickers: [],
  banner: null,
  owner_id: '...',
  application_id: '...',
  region: 'japan',
  afk_channel_id: null,
  afk_timeout: 300,
  system_channel_id: '...',
  widget_enabled: false,
  widget_channel_id: null,
  verification_level: 0,
  roles: [
    {
      id: '...',
      name: '@everyone',
      description: null,
      permissions: 104320577,
      position: 0,
      color: 0,
      hoist: false,
      managed: false,
      mentionable: false,
      icon: null,
      unicode_emoji: null,
      flags: 0,
      permissions_new: '...'
    }
  ],
  default_message_notifications: 0,
  mfa_level: 0,
  explicit_content_filter: 0,
  max_presences: null,
  max_members: 500000,
  max_stage_video_channel_users: 50,
  max_video_channel_users: 25,
  vanity_url_code: null,
  premium_tier: 0,
  premium_subscription_count: 0,
  system_channel_flags: 0,
  preferred_locale: 'en-US',
  rules_channel_id: null,
  safety_alerts_channel_id: null,
  public_updates_channel_id: null,
  hub_type: null,
  premium_progress_bar_enabled: false,
  latest_onboarding_question_id: null,
  nsfw: false,
  nsfw_level: 0,
  embed_enabled: false,
  embed_channel_id: null
}
```

