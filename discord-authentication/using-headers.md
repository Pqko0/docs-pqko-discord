---
description: Pqko-Discord Auth sets a couple of headers for you!
---

# Using headers

Pqko-Discord sends 4 headers these can be used how ever you wish

The required headers that you will receive are: \
&#x20;\- accessToken\
&#x20;\- refreshToken \
&#x20;\- logged (true || false)

If the user authorized with the "identify" scope you will also receive:\
&#x20;\- user

You can use this by doing:\
&#x20;\- req.\<headerName>

That's it!

