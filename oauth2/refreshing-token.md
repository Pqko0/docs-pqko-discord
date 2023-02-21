---
description: This is required after the access token expired
---

# Refreshing Token

And of course we have minimized the amount of code you require.

```javascript
OAuth2.refreshToken(refresh_token).then((x) => {
    console.log(x)
}).catch((x) => {
    console.log(x)
})
```

You will get the same response as the code validation.
