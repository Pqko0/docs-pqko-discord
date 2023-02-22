---
description: Preparing the login process
---

# Setting Login Page

Remember you can always use custom pages to make your website look better than sending raw text.

Now change the 3 dots in the "http://localhost:8000/..." to what ever your login page is

```javascript
app.get("/login", async (req, res) => {
    if(req.logged == true) return res.redirect("/dashboard")

    if(req.query.code) {
        const x = await auth.login(req, res)

        if(x.message == 1 && x.account == 1) {
            res.cookie("token", x.token)

            return res.redirect("/dashboard");
        } else return res.redirect(OAuth2Link)
    } else return res.redirect(OAuth2Link)
})
```

So it should look something like this

```javascript
const { client_id, client_secret, token } = require("./config.json") 
const OAuth2Link = "..."

const PqkoDiscord = require("pqko-discord")
const OAuth2 = new PqkoDiscord.OAuth2(client_id, client_secret, token, "http://localhost:8000/login")
const auth = new PqkoDiscord.Auth.DiscordAuth(OAuth2)

const express = require("express")
const app = express()

app.listen(8000, () => {
  console.log("🚀 Listening on port 8000!")
  console.log("http://localhost:8000")
})

app.use(PqkoDiscord.Auth.cookieparser())
app.use(auth.__express(OAuth2))

app.get("/", (req, res) => {
  res.send("Welcome to pqko-discord!")
})

app.get("/login", async (req, res) => {
    if(req.logged == true) return res.redirect("/dashboard")

    if(req.query.code) {
        const x = await auth.login(req, res)

        if(x.message == 1 && x.account == 1) {
            res.cookie("token", x.token)

            return res.redirect("/dashboard");
        } else return res.redirect(OAuth2Link)
    } else return res.redirect(OAuth2Link)
})
```
