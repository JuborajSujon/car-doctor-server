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

# How to set cookie in the server side

```code
res.cookie("token", token, {
          httpOnly: true,
          secure: false,
          sameSite: "none",
          maxAge: 1000 * 60 * 60 * 24 * 7,
        })
```

# How to set CORS in the server side

```code
app.use(cors({
  origin: ["http://localhost:5173"],
  credentials: true
}));
```

# How to set cookie in the client side with axios

in Axios use `withCredentials: true`
