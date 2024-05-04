# JWT Step By Step

1. install jsonwebtoken
   `npm install jsonwebtoken`
2. jwt.sing(payload, secret, { expiresIn: "1h" })
   `secret` = process.env.ACCESS_TOKEN_SECRET

```code
require('crypto').randomBytes(64).toString('hex')
```

3. token client

# How to store in the client side

1. use `localStorage` or `sessionStorage` to store the token - (XSS Vulnerable)
2. use react state to store the token
3. http only cookies

# Express cookie parser

1. install express cookie parser
   `npm install cookie-parser`
2. use `app.use(cookieParser())`
