---
description: There are 2 methods
---

# Setting Logout Page

You can use the one that comes with pqko-discord or the manual way.

Pqko-Discord:

```javascript
app.get("/logout", (req, res) => {
    if(req.logged == false) return res.redirect("/")

    auth.logout(req, res) // Passes nothing back
    return res.redirect("/")
})
```

Manual:

```javascript
app.get("/logout", (req, res) => {
    if(req.logged == false) return res.redirect("/")

    res.clearCookie("token")
    return res.redirect("/")
})
```
