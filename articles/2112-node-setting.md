---
title: "2112-node-setting"
emoji: "🎃"
type: "tech"
topics: ["nodejs"]
published: false
reviewed: done
---
# 2112-node-setting

## overview
- nodejs environment

## download
- nodejs
  - https://nodejs.org/en/download/
- nvm
  - https://github.com/coreybutler/nvm-windows/releases

## installation
- installerの指示にあわせて、Installする。
  
# environment
### nvm, node, npm
```
PS G:\workspace\ts-get-started> nvm version
1.1.8
PS G:\workspace\ts-get-started> nvm list

  * 16.13.0 (Currently using 64-bit executable)
PS G:\workspace\ts-get-started> node -v
v16.13.0
PS G:\workspace\ts-get-started> npm -v
8.1.0
PS G:\workspace\ts-get-started> npx -v
8.1.0
PS G:\workspace\ts-get-started>
```
- path 
```
PS G:\workspace\ts-get-started> $env:path -split ";" | oss | sls "nvm" , "node"

C:\Users\sakai\AppData\Roaming\nvm
C:\Program Files\nodejs
```

### yarn
- npmよりも高速なPackage Mananger 
  - https://classic.yarnpkg.com/lang/en/docs/install/#windows-stable
  - https://www.yoheim.net/blog.php?q=20170209
```
PS C:\Users\sakai> npm install --global yarn

added 1 package, and audited 2 packages in 6s

found 0 vulnerabilities
PS C:\Users\sakai> yarn --version
1.22.17
```

```
\PS C:\Users\sakai> npm list --global
C:\Users\sakai\AppData\Roaming\npm
+-- yarn@1.22.17
```

- yarn command list
  - https://classic.yarnpkg.com/en/docs/cli/

[end of file]