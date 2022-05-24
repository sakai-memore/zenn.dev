---
title: "2203-vanilla-js-vite-environment"
emoji: "👻"
type: "tech"
topics: []
published: false

---

# 2203-vanilla-js-vite-environment

## overview

- Create js vite environment for vanilla js.

## tool environment

```cmd
PS G:\workspace\hbs-templating> node --version
v16.13.0
PS G:\workspace\hbs-templating> npm --version
8.1.0
PS G:\workspace\hbs-templating> npx --version
8.1.0
```

## operations

### npm create vite@latest

- To scaffold vanille javascript project.

```cmd
PS G:\workspace\hbs-templating> npm create vite@latest
√ Project name: ... hbs-layouting
√ Select a framework: » vanilla
√ Select a variant: » vanilla

Scaffolding project in G:\workspace\hbs-templating\hbs-layouting...

Done. Now run:

  cd hbs-layouting
  npm install
  npm run dev

PS G:\workspace\hbs-templating> cd .\hbs-layouting\
PS G:\workspace\hbs-templating\hbs-layouting> ls

    Directory: G:\workspace\hbs-templating\hbs-layouting

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a---          27/02/2022    21:31            253 .gitignore
-a---          27/02/2022    21:31           1524 favicon.svg
-a---          27/02/2022    21:31            353 index.html
-a---          27/02/2022    21:31            177 main.js
-a---          05/03/2022    20:17            215 package.json
-a---          27/02/2022    21:31            199 style.css
```

### npm install

```cmd
PS G:\workspace\hbs-templating\hbs-layouting> npm install

added 14 packages, and audited 15 packages in 13s

4 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
```

#### package.json

```json
{
  "name": "hbs-layouting",
  "private": true,
  "version": "0.0.0",
  "scripts": {
    "dev": "vite",
    "build": "vite build",
    "preview": "vite preview"
  },
  "devDependencies": {
    "vite": "^2.8.0"
  }
}
```

### npmm run dev

```cmd
PS G:\workspace\hbs-templating\hbs-layouting> npm run dev

```

```console

  vite v2.8.6 dev server running at:

  > Local: http://localhost:3000/
  > Network: use `--host` to expose

  ready in 2515ms.

```

![vite hello](https://gyazo.com/4301322207eab6202175195c9a9c6ca8.png)