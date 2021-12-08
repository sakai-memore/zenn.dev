---
title: "2112-pwsh-setting"
emoji: "🦔"
type: "tech"
topics: ["pwsh", "powershell"]
published: false
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

[end of file]
