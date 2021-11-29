---
title: "2112-zenn-setting"
emoji: "🌟"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["setting"]
published: false
---
# 2112-zenn-setting

## overview
- keep notes on zenn.dev 

## setting
### git repository
- git config
```
PS G:\repos\zenn.dev> git config --global user.name "sakai-memore"
PS G:\repos\zenn.dev> git config --global user.email "mitsuru.sakai@gmail.com"

PS G:\repos\zenn.dev> git config --list
diff.astextplain.textconv=astextplain
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
http.sslbackend=openssl
http.sslcainfo=C:/Program Files/Git/mingw64/ssl/certs/ca-bundle.crt
core.autocrlf=true
core.fscache=true
core.symlinks=false
pull.rebase=false
credential.helper=manager-core
credential.https://dev.azure.com.usehttppath=true
init.defaultbranch=master
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
user.name=sakai-memore
user.email=mitsuru.sakai@gmail.com
core.repositoryformatversion=0
core.filemode=false
core.bare=false
core.logallrefupdates=true
core.symlinks=false
core.ignorecase=true
remote.origin.url=https://github.com/sakai-memore/zenn.dev.git
remote.origin.fetch=+refs/heads/*:refs/remotes/origin/*
```

### articles
```
PS G:\repos\zenn.dev> cd .\articles\
PS G:\repos\zenn.dev\articles> ls


    Directory: G:\repos\zenn.dev\articles


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        29/11/2021     15:47           1222 2112-zenn-setting.md
```

### zenn.dev
- GitHubリポジトリでZennのコンテンツを管理する
  + https://zenn.dev/zenn/articles/connect-to-github

-https://zenn.dev/dashboard/deploys 
![](https://i.gyazo.com/a046f547d4c28c9b9c282e101b0c04e5.png)

## push articles
### get personal access token
- https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token

## zenn-cli
- installation
  - https://zenn.dev/zenn/articles/zenn-cli-guide
- operation
  - https://zenn.dev/zenn/articles/zenn-cli-guide

```
$ npx zenn new:article --slug 2112-vuejs-setting --title 2112-vuejs-setting --type tech --emoji ✨ 
```

