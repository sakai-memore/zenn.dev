---
title: "2112-pwsh-setting"
emoji: "🦔"
type: "tech"
topics: ["pwsh", "powershell"]
published: false
reviewed: done
---
# 2112-pwsh-setting

## overview
- How to use pwsh, that is provides by Microsoft.

## reference
- https://docs.microsoft.com/ja-jp/powershell/scripting/install/installing-powershell-on-windows?view=powershell-7.1

## environment
- OS version, Pwsh version
```
PS G:\repos\zenn.dev> cmd winver
Microsoft Windows [Version 10.0.19042.1348]
(c) Microsoft Corporation. All rights reserved.

G:\repos\zenn.dev>
G:\repos\zenn.dev>exit
PS G:\repos\zenn.dev> $PSVersionTable

Name                           Value
----                           -----
PSVersion                      7.2.0
PSEdition                      Core
GitCommitId                    7.2.0
OS                             Microsoft Windows 10.0.19042
Platform                       Win32NT
PSCompatibleVersions           {1.0, 2.0, 3.0, 4.0…}
PSRemotingProtocolVersion      2.3
SerializationVersion           1.1.0.1
WSManStackVersion              3.0

```

- $Env:path
```
PS G:\repos\zenn.dev> $Env:path -split ";" | out-string -Stream | select-string "powershell"

C:\Program Files\PowerShell\7
C:\WINDOWS\System32\WindowsPowerShell\v1.0\
C:\Program Files\PowerShell\7\
G:\Users\sakai\OneDrive\Documents\WindowsPowerShell
```

- $Profile
```
PS G:\repos\zenn.dev> $Profile
G:\Users\sakai\OneDrive\Documents\PowerShell\Microsoft.PowerShell_profile.ps1
```

## Encoding on Powershell environment

- reference
  - https://dattesar.com/powershell-utf8/

## scoop

### reference
- https://scoop.sh/
- https://github.com/ScoopInstaller/Scoop/wiki
- https://qiita.com/OpenJNY/items/9783d6f2c9745da7d0d9
### installation
```
PS G:\workspace\ts-basic> Invoke-Expression (New-Object System.Net.WebClient).DownloadString("https://get.scoop.sh")
Initializing...
Downloading scoop...
Extracting...
Creating shim...
Downloading main bucket...
Extracting...
Adding ~\scoop\shims to your path.
'lastupdate' has been set to '2021-12-08T17:21:05.7195395+09:00'
Scoop was installed successfully!
Type 'scoop help' for instructions.

PS G:\workspace\ts-basic> scoop help
Usage: scoop <command> [<args>]

Some useful commands are:

alias       Manage scoop aliases
bucket      Manage Scoop buckets
cache       Show or clear the download cache
checkup     Check for potential problems
cleanup     Cleanup apps by removing old versions
config      Get or set configuration values
create      Create a custom app manifest
depends     List dependencies for an app
export      Exports (an importable) list of installed apps
help        Show help for a command
hold        Hold an app to disable updates
home        Opens the app homepage
info        Display information about an app
install     Install apps
list        List installed apps
prefix      Returns the path to the specified app
reset       Reset an app to resolve conflicts
search      Search available apps
status      Show status and check for new app versions
unhold      Unhold an app to enable updates
uninstall   Uninstall an app
update      Update apps, or Scoop itself
virustotal  Look for app's hash on virustotal.com
which       Locate a shim/executable (similar to 'which' on Linux)

Type 'scoop help <command>' to get help for a specific command.
PS G:\workspace\ts-basic> scoop list
There aren't any apps installed.
PS G:\workspace\ts-basic> scoop status
WARN  Scoop is out of date. Run 'scoop update' to get the latest changes.
PS G:\workspace\ts-basic> scoop update
Updating Scoop...
Updating 'main' bucket...
Checking repo... ok
The main bucket was added successfully.
Scoop was updated successfully!
PS G:\workspace\ts-basic>
```

[end of file]
