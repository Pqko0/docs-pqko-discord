---
description: Shows the minimal code to use this.
---

# Basic Setup

As long as you have the configuration file (JSON) correctly. This should be a copy paste.

Please remember the redirect\_uri will have to depend where your web server is found. Do remember they parse it through a query called "code" which will show how to automate it in the Discord Auth Section!

```javascript
const { token, client_id, client_secret } = require("./config.json")
const PqkoDiscord = require("pqko-discord")
const OAuth2 = new PqkoDiscord.OAuth2(token, client_id, client_secret, redirect_url)
```

That's all you need!
