---
title: "2112-git-environment"
emoji: "📝"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: []
published: false
---
# 2112-git-environment

## git for windows

## github desktop

## gibo
### reference
- https://github.com/simonwhitaker/gibo

### installation on Windows
```
PS G:\repos\zenn.dev> scoop update
Updating Scoop...
Updating 'main' bucket...
 * 8dd2758de neovim-nightly: Update to version 0.7.0-dev-688-g5abd7c2c1  5 minutes ago
Scoop was updated successfully!

PS G:\repos\zenn.dev> scoop install gibo
Installing 'gibo' (2.2.4) [64bit]
Downloading https://github.com/simonwhitaker/gibo/archive/2.2.4.zip (-1 B)...

Checking hash of 2.2.4.zip ... ok.
Extracting 2.2.4.zip ... done.
Linking ~\scoop\apps\gibo\current => ~\scoop\apps\gibo\2.2.4
Creating shim for 'gibo'.
'gibo' (2.2.4) was installed successfully!
PS G:\repos\zenn.dev> scoop list
Installed apps:

  gibo 2.2.4 [main]

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
```

### Typical usage
```
$ gibo dump Swift Xcode >> .gitignore
```