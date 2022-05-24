---
title: "2112-typescript-basic"
emoji: "⌨"
type: "tech"
topics: ["typescript"]
published: false
---
# 2112-typescript-basic

## overview
- typescriptの基礎を記述する。

## What typescript is ?
- javascriptに対して、Type systemを強化する仕組みを持つ。
- IDEと連携することで、Type systemをコーディング時に活用できる。

## environment
```
S G:\workspace\ts-basic> nvm list

  * 16.13.0 (Currently using 64-bit executable)
PS G:\workspace\ts-basic> node --version
v16.13.0
PS G:\workspace\ts-basic> npm list --global
C:\Users\sakai\AppData\Roaming\npm
+-- typescript@4.5.2
`-- yarn@1.22.17

PS G:\workspace\ts-basic> tsc --version
Version 4.5.2
```

```
PS G:\workspace> mkdir ts-basic

    Directory: G:\workspace

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d----          08/12/2021    16:50                ts-basic

PS G:\workspace> cd ts-basic
PS G:\workspace\ts-basic>
```

## initialization
### node project environment
```
PS G:\workspace\ts-basic> npm init
This utility will walk you through creating a package.json file.
It only covers the most common items, and tries to guess sensible defaults.

See `npm help init` for definitive documentation on these fields
and exactly what they do.

Use `npm install <pkg>` afterwards to install a package and
save it as a dependency in the package.json file.

Press ^C at any time to quit.
package name: (ts-basic)
version: (1.0.0)
description: typescript basic
entry point: (index.js)
test command:
git repository:
keywords: typescript, ts
author: memoru
license: (ISC) MIT
About to write to G:\workspace\ts-basic\package.json:

{
  "name": "ts-basic",
  "version": "1.0.0",
  "description": "typescript basic",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [
    "typescript",
    "ts"
  ],
  "author": "memoru",
  "license": "MIT"
}


Is this OK? (yes) yes
PS G:\workspace\ts-basic>
```


### tsc project environment

```
PS G:\workspace\ts-basic> tsc --init

Created a new tsconfig.json with:
                                                                                                                     TS
  target: es2016
  module: commonjs
  strict: true
  esModuleInterop: true
  skipLibCheck: true
  forceConsistentCasingInFileNames: true


You can learn more at https://aka.ms/tsconfig.json
```

### git environment
- gibo
```
PS G:\workspace\ts-basic> gibo help
gibo 2.2 by Simon Whitaker <sw@netcetera.org>
https://github.com/simonwhitaker/gibo

Fetches gitignore boilerplates from github.com/github/gitignore

Usage:
    gibo [command]

Example:
    gibo dump Python NotepadPP >> .gitignore

Options:
    dump expr...  Dump boilerplate(s) to stdout
    help          Display this help text
    list          List available boilerplates
    root          Show the directory where gibo stores its boilerplates
    search expr   Search inside boilerplates for expr
    update        Update list of available boilerplates
    version       Display current script version
PS G:\workspace\ts-basic> gibo dump typescript node vim > .gitignore
PS G:\workspace\ts-basic> ls

    Directory: G:\workspace\ts-basic

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a---          08/12/2021    17:49           2457 .gitignore
-a---          08/12/2021    16:54            274 package.json
-a---          08/12/2021    17:40          11101 tsconfig.json

```

- git
```
PS G:\workspace\ts-basic> git init
Initialized empty Git repository in G:/workspace/ts-basic/.git/
```

```
PS G:\workspace\ts-basic> git config --list --global
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
user.name=sakai-memore
user.email=mitsuru.sakai@gmail.com
```