---
title: "2112-zenn-setting"
emoji: "✨"
type: "tech"
topics: ["zenn"]
published: false
---
# 2112-zenn-setting

## overview
- keep notes and logs of tasks on zenn.dev 

## What is zenn.dev
- zenn.devは、IT Engineerのための、情報共有サイト。
  - https://zenn.dev/
- Communityの中で、情報発信していくことで、関連する情報と繋がれるというメリットを享受できる。
- ITエンジニアは、IT情報を、全世界のサイトをGoogleで検索しながら、知見を集めて、Engineeringを行っている。あるITタスクを、ある文脈で達成する際に、いくつかの知識を、総合的に、利用して、タスクを実施している。この際に、そのタスクで得た知見を、あとで使える形式で、保持しておくものである。
- で、自分がITタスクを達成するために、蓄積した知見は、他のITエンジニアと共有したいと考えている。ITエンジニアは、そういう生き物。
- zenn.devは、そのようなITエンジニアのニーズを支援するサイトといえる。
- zenn.devは、Github上のRepositoryに、Markdown形式で書いた文章を、zenn.devサイトと連携して、簡易に公開することが可能になっている。GitHub, MarkdownといったITエンジニアになじみのある環境で、知見を蓄積して、それを公開することができるので、エンジニアにはメリットが大きい。

## setting

### Create git repository
- GitHubにて、zenn.devと連携させるRepositoryを作成する。
- 当該のRepositoryを、Local PCと連携させる。

```
ni README.md
echo "# zenn.dev repository" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/sakai-memore/zenn.dev.git
git push -u origin main
```
#### reference
- https://newbedev.com/changing-powershell-s-default-output-encoding-to-utf-8



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
$ npx zenn new:article --slug 2112-zenn-setting --title 2112-zenn-setting --type tech --emoji ✨ 
```
[end of file]
