---
title: "2112-node-setting"
emoji: "🎃"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["nodejs"]
published: false
---
# 2112-node-setting

## overview
- nodejs environment

## download
- nodejs
  - https://nodejs.org/en/download/
- nvm
  - https://github.com/coreybutler/nvm-windows/releases

## environment
### nvm, node, npm
```
PS G:\repos\zenn.dev\articles> nvm version
1.1.8
PS G:\repos\zenn.dev\articles> nvm list

  * 16.13.0 (Currently using 64-bit executable)
PS G:\repos\zenn.dev\articles> node -v
v16.13.0
PS G:\repos\zenn.dev\articles> npm -v
8.1.0
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
- yarn command list
  - https://classic.yarnpkg.com/en/docs/cli/

[end of file]