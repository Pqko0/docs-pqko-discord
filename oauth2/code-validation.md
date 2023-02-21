---
description: Validate the receiving code from Discord OAuth2
---

# Code Validation

Of course, change the "code" to the code received from the web server

```javascript
OAuth2.codeValidation(code).then((x) => {
    console.log(x)
}).catch((x) => {
    console.log(x)
})
```

You can also use it in the asynchronous form and this should pass back these following JSON

```json
{
  "access_token": '...',
  "expires_in": 604800,
  "refresh_token": '...',
  "scope": '...',
  "token_type": 'Bearer'
}
```
