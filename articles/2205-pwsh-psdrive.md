# 2205-pwsh-psdrive
#pwsh

## overview
- psdrive

## code
### dir Env:
```powershell
PS C:\Users\sakai> dir Env:

Name                           Value
----                           -----
ALLUSERSPROFILE                C:\ProgramData
APPDATA                        C:\Users\sakai\AppData\Roaming
ChocolateyInstall              C:\ProgramData\chocolatey
ChocolateyLastPathUpdate       132826589735267677
CommonProgramFiles             C:\Program Files\Common Files
CommonProgramFiles(x86)        C:\Program Files (x86)\Common Files
CommonProgramW6432             C:\Program Files\Common Files
COMPUTERNAME                   DESKTOP-2RE0MH8
ComSpec                        C:\WINDOWS\system32\cmd.exe
DriverData                     C:\Windows\System32\Drivers\DriverData
HOMEDRIVE                      C:
HOMEPATH                       \Users\sakai
LOCALAPPDATA                   C:\Users\sakai\AppData\Local
LOGONSERVER                    \\DESKTOP-2RE0MH8
NUMBER_OF_PROCESSORS           4
NVM_HOME                       C:\Users\sakai\AppData\Roaming\nvm
NVM_SYMLINK                    C:\Program Files\nodejs
OneDrive                       G:\Users\sakai\OneDrive
OneDriveConsumer               G:\Users\sakai\OneDrive
OS                             Windows_NT
Path                           C:\Program Files\PowerShell\7;C:\Python310\Scripts\;C:\Python310\;C:\Program Files (x86…
PATHEXT                        .COM;.EXE;.BAT;.CMD;.VBS;.VBE;.JS;.JSE;.WSF;.WSH;.MSC;.PY;.PYW;.CPL
POWERSHELL_DISTRIBUTION_CHANN… MSI:Windows 10 Pro
PROCESSOR_ARCHITECTURE         AMD64
PROCESSOR_IDENTIFIER           Intel64 Family 6 Model 92 Stepping 10, GenuineIntel
PROCESSOR_LEVEL                6
PROCESSOR_REVISION             5c0a
ProgramData                    C:\ProgramData
ProgramFiles                   C:\Program Files
ProgramFiles(x86)              C:\Program Files (x86)
ProgramW6432                   C:\Program Files
PSModulePath                   G:\Users\sakai\OneDrive\Documents\PowerShell\Modules;C:\Program Files\PowerShell\Module…
PUBLIC                         C:\Users\Public
SystemDrive                    C:
SystemRoot                     C:\WINDOWS
TEMP                           C:\Users\sakai\AppData\Local\Temp
TMP                            C:\Users\sakai\AppData\Local\Temp
USERDOMAIN                     DESKTOP-2RE0MH8
USERDOMAIN_ROAMINGPROFILE      DESKTOP-2RE0MH8
USERNAME                       sakai
USERPROFILE                    C:\Users\sakai
windir                         C:\WINDOWS
WSLENV                         WT_SESSION::WT_PROFILE_ID
WT_PROFILE_ID                  {574e775e-4f2a-5b96-ac1e-a2962a402336}
WT_SESSION                     1a303f9d-0bd8-4ad8-b28f-a156347dafed
```

#### echo (Write-Output)
```powershell
PS C:\Users\sakai> Get-Alias | out-string -stream | select-string 'Write'

Alias           echo -> Write-Output
Alias           write -> Write-Output

PS C:\Users\sakai> echo $Env:APPDATA
C:\Users\sakai\AppData\Roaming

```

#### $Env:path -Split ";"
```powershell
PS C:\Users\sakai> $Env:Path -Split ";"
C:\Program Files\PowerShell\7
C:\Python310\Scripts\
C:\Python310\
C:\Program Files (x86)\Intel\TXE Components\iCLS\
C:\Program Files\Intel\TXE Components\iCLS\
C:\WINDOWS\system32
C:\WINDOWS
C:\WINDOWS\System32\Wbem
C:\WINDOWS\System32\WindowsPowerShell\v1.0\
C:\WINDOWS\System32\OpenSSH\
C:\Program Files\Intel\TXE Components\DAL\
C:\Program Files (x86)\Intel\TXE Components\DAL\
C:\Program Files\Intel\TXE Components\IPT\
C:\Program Files (x86)\Intel\TXE Components\IPT\
C:\Program Files\Intel\WiFi\bin\
C:\Program Files\Common Files\Intel\WirelessCommon\
C:\Program Files\Git\cmd
C:\Program Files\dotnet\
C:\ProgramData\chocolatey\bin
C:\Users\sakai\AppData\Roaming\nvm
C:\Program Files\nodejs
C:\Program Files\Microsoft VS Code\bin
C:\Program Files\PowerShell\7\
C:\Program Files (x86)\WinMerge
C:\PROGRA~1\JPKI
C:\Program Files (x86)\Common Files\Sony Shared\FeliCaLibrary
C:\Program Files\Common Files\Sony Shared\FeliCaLibrary
C:\Users\sakai\scoop\shims
C:\Users\sakai\miniconda3
C:\Users\sakai\miniconda3\Library\mingw-w64\bin
C:\Users\sakai\miniconda3\Library\usr\bin
C:\Users\sakai\miniconda3\Library\bin
C:\Users\sakai\miniconda3\Scripts
C:\Users\sakai\AppData\Local\Microsoft\WindowsApps
G:\Users\sakai\Desktop
G:\Users\sakai\Desktop\tools
C:\Users\sakai\AppData\Local\GitHubDesktop\bin
G:\Users\sakai\OneDrive\Documents\WindowsPowerShell
C:\Program Files (x86)\sakura
C:\Users\sakai\AppData\Roaming\npm
C:\Program Files\PostgreSQL\14\bin
C:\Users\sakai\AppData\Roaming\Haroo Studio\Haroopad
C:\Program Files\Vim\vim82
C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Python 3.10
C:\Program Files\Typora
G:\Users\sakai\Downloads\HBuilderX.3.4.7.20220422\HBuilderX
G:\Users\sakai\Downloads\wzme118

```

### dir Variable:

```powershell
PS C:\Users\sakai> dir Variable:

Name                           Value
----                           -----
?                              False
^                              dir
$                              Varable:
args                           {}
ConfirmPreference              High
DebugPreference                SilentlyContinue
EnabledExperimentalFeatures    {}
Error                          {Cannot find drive. A drive with the name 'Varable' does not exist.}
ErrorActionPreference          Continue
ErrorView                      ConciseView
ExecutionContext               System.Management.Automation.EngineIntrinsics
false                          False
FormatEnumerationLimit         4
HOME                           C:\Users\sakai
Host                           System.Management.Automation.Internal.Host.InternalHost
InformationPreference          SilentlyContinue
input                          System.Collections.ArrayList+ArrayListEnumeratorSimple
IsCoreCLR                      True
IsLinux                        False
IsMacOS                        False
IsWindows                      True
MaximumHistoryCount            4096
MyInvocation                   System.Management.Automation.InvocationInfo
NestedPromptLevel              0
null
OutputEncoding                 System.Text.UTF8Encoding
PID                            8728
PROFILE                        G:\Users\sakai\OneDrive\Documents\PowerShell\Microsoft.PowerShell_profile.ps1
ProgressPreference             Continue
PSBoundParameters              {}
PSCommandPath
PSCulture                      en-GB
PSDefaultParameterValues       {}
PSEdition                      Core
PSEmailServer
PSHOME                         C:\Program Files\PowerShell\7
PSScriptRoot
PSSessionApplicationName       wsman
PSSessionConfigurationName     http://schemas.microsoft.com/powershell/Microsoft.PowerShell
PSSessionOption                System.Management.Automation.Remoting.PSSessionOption
PSStyle                        System.Management.Automation.PSStyle
PSUICulture                    en-US
PSVersionTable                 {PSVersion, PSEdition, GitCommitId, OS…}
PWD                            C:\Users\sakai
ShellId                        Microsoft.PowerShell
StackTrace
true                           True
VerbosePreference              SilentlyContinue
WarningPreference              Continue
WhatIfPreference               False
```





