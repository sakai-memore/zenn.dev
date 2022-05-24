---
title: "# 2112-nestjs-get-started"
emoji: "🐈"
type: "tech" 
topics: []
published: false
reviewed: "in progress"

---

# 2112-nestjs-get-started

## initialize development environment

```
S G:\workspace> mkdir nest-get-started

    Directory: G:\workspace

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d----          17/12/2021    11:31                nest-get-started

PS G:\workspace> cd .\nest-get-started\
PS G:\workspace\nest-get-started> git init
Initialized empty Git repository in G:/workspace/nest-get-started/.git/
PS G:\workspace\nest-get-started> gibo dump vim node ts >> .gitignore
PS G:\workspace\nest-get-started> ls

    Directory: G:\workspace\nest-get-started

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a---          17/12/2021    11:32           2449 .gitignore
```


## installation

```
PS G:\workspace\nest-get-started> npm install --global @nestjs/cli

added 257 packages, and audited 258 packages in 57s

37 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
PS G:\workspace\nest-get-started> cd ..
PS G:\workspace> nest --version
8.1.6
```
## Get started

### nest new nest-get-started

```
PS G:\workspace> nest new nest-get-started
⚡  We will scaffold your app in a few seconds..

CREATE nest-get-started/.eslintrc.js (631 bytes)
CREATE nest-get-started/.prettierrc (51 bytes)
CREATE nest-get-started/nest-cli.json (64 bytes)
CREATE nest-get-started/package.json (2005 bytes)
CREATE nest-get-started/README.md (3339 bytes)
CREATE nest-get-started/tsconfig.build.json (97 bytes)
CREATE nest-get-started/tsconfig.json (546 bytes)
CREATE nest-get-started/src/app.controller.spec.ts (617 bytes)
CREATE nest-get-started/src/app.controller.ts (274 bytes)
CREATE nest-get-started/src/app.module.ts (249 bytes)
CREATE nest-get-started/src/app.service.ts (142 bytes)
CREATE nest-get-started/src/main.ts (208 bytes)
CREATE nest-get-started/test/app.e2e-spec.ts (630 bytes)
CREATE nest-get-started/test/jest-e2e.json (183 bytes)

? Which package manager would you ❤️  to use? npm
√ Installation in progress... ☕

🚀  Successfully created project nest-get-started
👉  Get started with the following commands:

$ cd nest-get-started
$ npm run start


                          Thanks for installing Nest 🙏
                 Please consider donating to our open collective
                        to help us maintain this package.


               🍷  Donate: https://opencollective.com/nest

PS G:\workspace>
```

### npm run start

```
PS G:\workspace> cd .\nest-get-started\
PS G:\workspace\nest-get-started> npm run start

> nest-get-started@0.0.1 start
> nest start

[Nest] 17548  - 17/12/2021, 12:21:23     LOG [NestFactory] Starting Nest application...
[Nest] 17548  - 17/12/2021, 12:21:23     LOG [InstanceLoader] AppModule dependencies initialized +138ms
[Nest] 17548  - 17/12/2021, 12:21:23     LOG [RoutesResolver] AppController {/}: +20ms
[Nest] 17548  - 17/12/2021, 12:21:23     LOG [RouterExplorer] Mapped {/, GET} route +10ms
[Nest] 17548  - 17/12/2021, 12:21:23     LOG [NestApplication] Nest application successfully started +10ms

```
![screenshot of localhost](https://i.gyazo.com/ea6eacf6606338577ccce6e9fe68c42c.png)
