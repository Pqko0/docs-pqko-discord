---
description: This will require the access token.
---

# Get User

This requires the identify scope and to get the user email you will also require the email scope.

```javascript
OAuth2.getUser(access_token).then((x) => {
    console.log(x)
}).catch((x) => {
    console.log(x)
})
```

This is the response you should receive.&#x20;

```json
{
  "id": '...',
  "username": '...',
  "display_name": null,
  "avatar": '...',
  "avatar_decoration": null,
  "discriminator": '...',
  "public_flags": 64,
  "flags": 64,
  "banner": null,
  "banner_color": '...',
  "accent_color": ...,
  "locale": '...',
  "mfa_enabled": false,
  "premium_type": 0,
  "email": '...',
  "verified": true
}
```
