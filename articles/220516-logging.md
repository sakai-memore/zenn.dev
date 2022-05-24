---
title: "220516-logging"
emoji: "🐙"
type: "idea"
topics: ["logging"]
published: false
createDate: "220516-0623"

---

#2205 #logging

# 220516-logging :

## pwsh
#pwsh 
### hello world
```powershell
PS C:\Users\sakai> "Hello, world!"
Hello, world!
PS C:\Users\sakai> $msg = "Powershell"
PS C:\Users\sakai> dir Env:

Name                           Value
----                           -----
ALLUSERSPROFILE                C:\ProgramData
APPDATA                        C:\Users\sakai\AppData\Roaming
ChocolateyInstall              C:\ProgramData\chocolatey
ChocolateyLastPathUpdate       132970419145927292
ChocolateyToolsLocation        C:\tools
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
Path                           C:\Program Files\PowerShell\7;C:\Python310\Scripts\;C:\Python310\;…
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
PSModulePath                   G:\Users\sakai\OneDrive\Documents\PowerShell\Modules;C:\Program Fi…
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
WT_SESSION                     9955b427-91e0-4d5d-a430-7b524d4ffd06

PS C:\Users\sakai> dir Variable:

Name                           Value
----                           -----
?                              True
^                              dir
$                              Env:
args                           {}
ConfirmPreference              High
DebugPreference                SilentlyContinue
EnabledExperimentalFeatures    {}
Error                          {}
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
msg                            Powershell
MyInvocation                   System.Management.Automation.InvocationInfo
NestedPromptLevel              0
null
OutputEncoding                 System.Text.UTF8Encoding
PID                            14140
PROFILE                        G:\Users\sakai\OneDrive\Documents\PowerShell\Microsoft.PowerShell_…
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

PS C:\Users\sakai> dir Variable: | out-string -stream | sls "msg"

msg                            Powershell

PS C:\Users\sakai> $HOME
C:\Users\sakai
PS C:\Users\sakai> $PWD

Path
----
C:\Users\sakai

PS C:\Users\sakai> $PWD | gm

   TypeName: System.Management.Automation.PathInfo

Name         MemberType Definition
----         ---------- ----------
Equals       Method     bool Equals(System.Object obj)
GetHashCode  Method     int GetHashCode()
GetType      Method     type GetType()
ToString     Method     string ToString()
Drive        Property   System.Management.Automation.PSDriveInfo Drive {get;}
Path         Property   string Path {get;}
Provider     Property   System.Management.Automation.ProviderInfo Provider {get;}
ProviderPath Property   string ProviderPath {get;}

PS C:\Users\sakai> 'Hello, ${msg}!!'
Hello, ${msg}!!
PS C:\Users\sakai> "Hello, ${msg}!!"
Hello, Powershell!!
PS C:\Users\sakai> echo "Hello, ${msg}!!"
Hello, Powershell!!
PS C:\Users\sakai>

```

```powershell
PS C:\Users\sakai> $Env:path -split ";"
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
C:\Program Files (x86)\WinMerge
C:\PROGRA~1\JPKI
C:\Program Files (x86)\Common Files\Sony Shared\FeliCaLibrary
C:\Program Files\Common Files\Sony Shared\FeliCaLibrary
C:\Program Files\PowerShell\7\
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
C:\tools\dart-sdk\bin
C:\Users\sakai\AppData\Roaming\Pub\Cache\bin
PS C:\Users\sakai>
```

## typescript
#typescrpt #deno

```bat
PS C:\Users\sakai> tsc --version
Version 4.5.2
PS C:\Users\sakai> deno --version
deno 1.16.3 (release, x86_64-pc-windows-msvc)
v8 9.7.106.5
typescript 4.4.2
PS G:\workspace\22AA> yarn --version
1.22.17
```

### npm create vite@latest
```
PS G:\workspace\22AA> npm create vite@latest
Need to install the following packages:
  create-vite@latest
Ok to proceed? (y) y
√ Project name: ... vite-project
√ Select a framework: » vanilla
√ Select a variant: » vanilla-ts

Scaffolding project in G:\workspace\22AA\vite-project...

Done. Now run:

  cd vite-project
  npm install
  npm run dev

npm notice
npm notice New minor version of npm available! 8.7.0 -> 8.10.0
npm notice Changelog: https://github.com/npm/cli/releases/tag/v8.10.0
npm notice Run npm install -g npm@8.10.0 to update!
npm notice
PS G:\workspace\22AA>
```

## dart create -t console cli
```console
PS G:\workspace\22AA> dart --version
Dart SDK version: 2.17.0 (stable) (Mon May 9 10:36:47 2022 +0200) on "windows_x64"
PS G:\workspace\22AA> dart create -t console cli
Creating cli using template console...

  .gitignore
  analysis_options.yaml
  CHANGELOG.md
  pubspec.yaml
  README.md
  bin\cli.dart
  lib\cli.dart
  test\cli_test.dart

Running pub get...
  Resolving dependencies...
  Downloading lints 2.0.0...
  Downloading test 1.21.1...
  Downloading test_core 0.4.13...
  Downloading test_api 0.4.9...
  Downloading stream_channel 2.1.0...
  Downloading stack_trace 1.10.0...
  Downloading shelf_packages_handler 3.0.0...
  Downloading pool 1.5.0...
  Downloading boolean_selector 2.1.0...
  Downloading source_maps 0.10.10...
  Downloading source_map_stack_trace 2.1.0...
  Downloading matcher 0.12.11...
  Downloading term_glyph 1.2.0...
  Downloading webkit_inspection_protocol 1.0.1...
  Downloading typed_data 1.3.1...
  Downloading shelf_web_socket 1.0.1...
  Downloading shelf_static 1.1.0...
  Downloading http_parser 4.0.0...
  Downloading path 1.8.1...
  Downloading package_config 2.0.2...
  Downloading node_preamble 2.0.1...
  Downloading js 0.6.4...
  Downloading collection 1.16.0...
  Downloading string_scanner 1.1.1...
  Downloading convert 3.0.1...
  Downloading yaml 3.1.1...
  Downloading web_socket_channel 2.2.0...
  Downloading io 1.0.3...
  Downloading http_multi_server 3.2.0...
  Downloading glob 2.0.2...
  Downloading frontend_server_client 2.1.2...
  Downloading logging 1.0.2...
  Downloading mime 1.0.2...
  Downloading charcode 1.3.1...
  Downloading crypto 3.0.2...
  Downloading source_span 1.9.0...
  Downloading shelf 1.3.0...
  Downloading analyzer 4.0.0...
  Downloading meta 1.7.0...
  Downloading _fe_analyzer_shared 39.0.0...
  Downloading watcher 1.0.1...
  Downloading pub_semver 2.1.1...
  Downloading file 6.1.2...
  Downloading args 2.3.1...
  Downloading coverage 1.3.1...
  Downloading vm_service 8.3.0...
  Downloading async 2.9.0...
  Changed 47 dependencies!

Created project cli in cli! In order to get started, run the following commands:

  cd cli
  dart run

PS G:\workspace\22AA> cd
PS C:\Users\sakai> g:
PS G:\workspace\22AA> ls

    Directory: G:\workspace\22AA

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d----          04/04/2022    19:19                bootstrap-template
d----          02/04/2022    21:57                bpmn-js-advanced
d----          16/05/2022    17:25                cli
d----          08/04/2022    15:14                jquery-sample
d----          05/04/2022    15:43                lit-sample
d----          12/03/2022    09:17                node-get-started
d----          04/04/2022    13:50                svelte-sample
d----          07/04/2022    09:06                vanilla-sample
d----          16/05/2022    16:16                vite-project
d----          05/04/2022    16:47                web-component-sample

PS G:\workspace\22AA> cd cli
PS G:\workspace\22AA\cli> ls

    Directory: G:\workspace\22AA\cli

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d----          16/05/2022    17:25                .dart_tool
d----          16/05/2022    17:25                bin
d----          16/05/2022    17:25                lib
d----          16/05/2022    17:25                test
-a---          16/05/2022    17:25            113 .gitignore
-a---          16/05/2022    17:25           5119 .packages
-a---          16/05/2022    17:25           1038 analysis_options.yaml
-a---          16/05/2022    17:25             29 CHANGELOG.md
-a---          16/05/2022    17:25           7596 pubspec.lock
-a---          16/05/2022    17:25            233 pubspec.yaml
-a---          16/05/2022    17:25            122 README.md

PS G:\workspace\22AA\cli> dart run
Building package executable...
Built cli:cli.
Hello world: 42!
PS G:\workspace\22AA\cli> dart run
Building package executable...
Built cli:cli.
Hello world: 42!
PS G:\workspace\22AA\cli> explorer .
PS G:\workspace\22AA\cli> dart run
Building package executable...
Built cli:cli.
Hello world: 80!
PS G:\workspace\22AA\cli> dart run
Building package executable...
Built cli:cli.
Hello world: 80!
PS G:\workspace\22AA\cli>
```

## Chiebukuro
### Q: 負債を減らすメリットは何か
### Answer：
日本政府（＋日本銀行）は、管理通貨制度のもとで、市中にある日本円の量を適正にコントロールしている立場です。 市中にあるおカネは、勝手に、増えたり、減ったりしないです。誰かが適正にコントロールしています。つまり、政府は、市中にある日本円が、適正になるように、おカネを増やしたり、おカネを減らしたりしています。

市中にあるおカネは、紙幣が７％で、預金通貨が９３％です。 

紙幣は、日本銀行の負債です。 
預金通貨は、市中の経済主体の負債です。 

おカネは、負債の形式で、存在しています。 

国の負債とは、日本銀行の負債と、市中の経済主体の負債を、合計したものを指します。 

紙幣（日銀券）は、日本銀行の負債であり、日本銀行に、日本銀行券を持っていくと、おカネと交換してくれます。日本銀行券には、償還期限はないですし、利子もつきません。（金本位制の場合は、金ゴールドと交換してくれます） 

預金通貨は、市中の経済主体の負債であり、対応する経済主体に、借金証文をもっていくと、おカネ（紙幣）と交換してくれます。借金証文には、償還期限があり、利子もつきます。 

預金通貨は、民間銀行が、市中の経済主体の返済能力（生産能力）を査定して、担保を取るなどして、ゼロから生み出すおカネです。民間銀行のMoney Creationといいます。借金証文と紐づけて、その発生から返済（消滅）まで管理しています。 

＞国？政府？の負債をこれから先少しでも減らしていけたらどんなメリットが生まれますか？ 

＝＞国の負債を減らすというのは、預金通貨を減らすか、紙幣を減らすかのどちらかです。つまり、マネーを減らすということです。 

＝＞政府の負債を減らすというのは、政府の借金証文を返済して、預金通貨を減らすということです。つまり、マネーが減ります。 

日本政府は、借金証文を発行して、日本円を確保して、市中にバラまいています。バラまいた日本円は、日本国内でしか使えないため、市中で使われ、流通し、蓄積されます。消えてなくなりません。政府が、借金証文を返済するとなくなります。 

日本政府は、日本円を市中にバラまいていますが、その日本円を、市中にバラまいた分だけ、回収する権限を持ちます。徴税権と言います。日本政府が、自分でバラまいた分を、バラまいた分だけ回収しても、何の問題もありません。 

日本政府は、日本円を市中にバラまいていますが、その日本円を、市中にバラまいた分だけ、回収していません。その回収せずに、市中に残っている分が、国債発行残高となります。回収する前提で、借金証文と紐づけて、その返済（消滅）を管理しています。 

日本政府は、日本円を市中にバラまいていますが、その日本円を、市中にバラまいた分だけ、回収していないのは、そのおカネが、市中の金融資産になっているからです。日本政府は、資本主義経済を運営するにあたり、私有財産を尊重しているため、市中の私有財産から、無理やり、回収することをしていません。わざわざ、市中におカネを残すように運用しています。 

日本政府が、市中にバラまいているおカネは、統計上、家計の金融資産になっています。市中のおカネは、１２００兆円あり、毎年、３５兆円ていど、継続的に、増えています。 

資本主義経済では、マネーは膨張することで、経済運営が安定します。ピケティ教授が、ｇ＜ｒの式で、言及されています。 日本政府は、資本主義経済を、安定的に運用するために、毎年、３５兆円ていど、市中のマネーの量（マネーストック）が増えるように、コントロールしています。 

市中のおカネは、勝手に湧いて出てこないので、日本政府と日本銀行が、管理通貨制度のもと、その量を適正にコントロールしています。 

市中のおカネを増やすには、民間銀行のMoney Creationを適正に増やす必要があります。 市中のおカネを減らすには、民間銀行におカネを返済することになります。市中にあるおカネの９５％は、国債をベースにMoney Creationされています。なので、市中のおカネを減らすには、政府が国債を返済することで、適正に減らすことができます。これを、ＰＢ黒字化と言います。 

日本政府と日本銀行は、マネーの量を適正量にし、マネーの流動性を適正にするようにして、マネーを制御しています。その指標は、失業率、インフレ率、ＧＤＰの前年比です。 当該の指標を監視しながら、マネーが適正になるようにするのが、日本政府と日本銀行の役割です。 

日本経済の場合、マネーストックは、毎年、約３５兆円、増加することで、安定しています。毎年、以下の式が成立しています。 

マネーストックの３５兆円の増分＝民間銀行の貸出増分
＝民間企業の借入増分＋家計の借入増分＋日本政府の借入増分 

現在の日本経済では、民間の経済活動だけでは、民間銀行の貸出が増えず、適正量、Money Creationされていません。なので、政府が、民間銀行のMoney Creationを促すように、毎年、２０～４０兆円の借金をして、民間銀行のMoney Creationを、下支えしています。政府は、下支えしないと、民間銀行の経営がうまくいかず、倒産します。民間銀行が倒産しないということは、マネーストックが適正に増えているという感じです。 

日本経済では、家計の消費性向が、７０～８０％で、家計は、収入の２０～３０％を貯蓄に回す傾向があります。家計は、老後２０００万円問題をクリアするため、粛々と、貯蓄をしています。 

日本経済全体でみると、家計が消費せずに、貯蓄に回した分を、誰かが消費量を増やさないと、ＧＤＰが全体として、マイナスになります。 

成長期は、家計が消費にしない分を、 
民間企業が、設備投資したり 
家計が、住宅ローンなどの住宅投資をしたり 
政府が、社会インフラ投資したり 
したので、政府は、借金を増やさなくても、問題なかったです。 

が、１９９８年以降は、 生産年齢人口が減り、 不良債権処理で、流動的なマネーが、１００兆円ほど減ったため、 民間の経済活動では、適正にMoney Creationされない状況です。で、政府が、その減った分を補填することで、ＧＤＰがマイナスにならないようにしています。 

＞もしも国？政府？の負債をこれから先少しでも減らしていけたらどんなメリットが生まれますか？ 

＝＞管理通貨制度のもと、マネーは負債として存在していますので、負債を減らすと、マネーが減ります。マネーの量が適正でない場合は、PＢ黒字化をして、市中のマネーを、国債の返済により減らすことになります。 

つまり、マネーの量が適正でない場合は、負債を減らすメリットがあります。

適正でない場合とは、失業率、インフレ率、ＧＤＰ前年比の指標が、基準値をプラスにオーバーしているか、マイナスにオーバーしている状況です。 

状況にあわせて、減らせばよいです。
