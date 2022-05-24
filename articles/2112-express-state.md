---
title: "2112-express-state
emoji: "🚈"
type: "tech"
topics: ["nodejs", "expressjs", "express-state"]
published: false
reviewed: false
---
# 2112-express-state
## reference
- https://github.com/YahooArchive/express-state#readme
## overview
- `Express state` is designed to make it easy to share configuration and state data from the server to the client. It can be used to share any data that needs to be available to the client-side js code of the frontend apps. e.g. the current user info, a CSRF token, model data, routes, etc.


## installation
- npm install
```
PS G:\workspace\boot-sample> npm install express-state

added 3 packages, and audited 59 packages in 4s

found 0 vulnerabilities
PS G:\workspace\boot-sample> npm install express-session

added 6 packages, and audited 65 packages in 3s

1 package is looking for funding
  run `npm fund` for details

found 0 vulnerabilities
PS G:\workspace\boot-sample> npm install csrf

added 3 packages, and audited 68 packages in 4s

1 package is looking for funding
  run `npm fund` for details

found 0 vulnerabilities
```
- npm list
```
PS G:\workspace\boot-sample> npm list
ejsboots@0.0.0 G:\workspace\boot-sample
+-- bootstrap-icons@1.7.2
+-- cookie-parser@1.4.4
+-- csrf@3.1.0
+-- debug@2.6.9
+-- ejs@2.6.2
+-- express-ejs-layouts@2.5.0
+-- express-session@1.17.2
+-- express-state@2.0.0
+-- express@4.16.4
+-- http-errors@1.6.3
`-- morgan@1.9.1

```

[end of file]