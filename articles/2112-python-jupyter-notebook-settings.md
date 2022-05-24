---
title: "2112-python-jupyter-notebook-settings"
emoji: "📘"
type: "tech"
topics: ["jupyter notebook"]
published: false
reviewed: false
---

# 2112-python-jupyter-notebook-settings :

## overview :
- To use python and this ecosystems, set PC environment for effective and proper use.


## environment :

```cmd
G:\workspace>cd jupnote

G:\workspace\jupnote>dir
 Volume in drive G is New Volume
 Volume Serial Number is A0B0-51B7

 Directory of G:\workspace\jupnote

27/12/2021  09:38    <DIR>          .
27/12/2021  09:38    <DIR>          ..
               0 File(s)              0 bytes
               2 Dir(s)  98,243,792,896 bytes free

G:\workspace\jupnote>conda env list
# conda environments:
#
base                  *  C:\Users\sakai\miniconda3
jup                      C:\Users\sakai\miniconda3\envs\jup


G:\workspace\jupnote>conda activate jup

(jup) G:\workspace\jupnote>conda env list
# conda environments:
#
base                     C:\Users\sakai\miniconda3
jup                   *  C:\Users\sakai\miniconda3\envs\jup

(jup) G:\workspace\jupnote>pwsh
PowerShell 7.2.1
Copyright (c) Microsoft Corporation.

https://aka.ms/powershell
Type 'help' to get help.

PS G:\workspace\jupnote> $Env:path -split ";" | oss | sls "conda"

C:\Users\sakai\miniconda3\envs\jup
C:\Users\sakai\miniconda3\envs\jup\Library\mingw-w64\bin
C:\Users\sakai\miniconda3\envs\jup\Library\usr\bin
C:\Users\sakai\miniconda3\envs\jup\Library\bin
C:\Users\sakai\miniconda3\envs\jup\Scripts
C:\Users\sakai\miniconda3\envs\jup\bin
C:\Users\sakai\miniconda3\condabin
C:\Users\sakai\miniconda3
C:\Users\sakai\miniconda3\Library\mingw-w64\bin
C:\Users\sakai\miniconda3\Library\usr\bin
C:\Users\sakai\miniconda3\Library\bin
C:\Users\sakai\miniconda3\Scripts

PS G:\workspace\jupnote> exit

(jup) G:\workspace\jupnote>
```

## jupyter notebook

```cmd
(jup) G:\workspace\jupnote>jupyter notebook
[I 10:02:32.639 NotebookApp] Serving notebooks from local directory: G:\workspace\jupnote
[I 10:02:32.640 NotebookApp] Jupyter Notebook 6.4.6 is running at:
[I 10:02:32.642 NotebookApp] http://localhost:8888/?token=f0cb1d5cc823cf0e201ab48da24cb2ee88e83edfd13ab3f3
[I 10:02:32.643 NotebookApp]  or http://127.0.0.1:8888/?token=f0cb1d5cc823cf0e201ab48da24cb2ee88e83edfd13ab3f3
[I 10:02:32.644 NotebookApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
[C 10:02:33.024 NotebookApp]

    To access the notebook, open this file in a browser:
        file:///C:/Users/sakai/AppData/Roaming/jupyter/runtime/nbserver-14204-open.html
    Or copy and paste one of these URLs:
        http://localhost:8888/?token=f0cb1d5cc823cf0e201ab48da24cb2ee88e83edfd13ab3f3
     or http://127.0.0.1:8888/?token=f0cb1d5cc823cf0e201ab48da24cb2ee88e83edfd13ab3f3
```


## jupyter lab

### installation

```cmd
(jup) G:\workspace\jupnote>conda install -c conda-forge jupyterlab
Collecting package metadata (current_repodata.json): done
Solving environment: done


==> WARNING: A newer version of conda exists. <==
  current version: 4.10.3
  latest version: 4.11.0

Please update conda by running

    $ conda update -n base -c defaults conda



## Package Plan ##

  environment location: C:\Users\sakai\miniconda3\envs\jup

  added / updated specs:
    - jupyterlab


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    anyio-3.4.0                |  py310h5588dad_0         154 KB  conda-forge
    argon2-cffi-21.1.0         |  py310he2412df_2          50 KB  conda-forge
    async_generator-1.10       |             py_0          18 KB  conda-forge
    attrs-21.2.0               |     pyhd8ed1ab_0          44 KB  conda-forge
    babel-2.9.1                |     pyh44b312d_0         6.2 MB  conda-forge
    backcall-0.2.0             |     pyh9f0ad1d_0          13 KB  conda-forge
    backports-1.0              |             py_2           4 KB  conda-forge
    backports.functools_lru_cache-1.6.4|     pyhd8ed1ab_0           9 KB  conda-forge
    bleach-4.1.0               |     pyhd8ed1ab_0         121 KB  conda-forge
    brotlipy-0.7.0             |py310he2412df_1003         370 KB  conda-forge
    ca-certificates-2021.10.8  |       h5b45459_0         176 KB  conda-forge
    certifi-2021.10.8          |  py310h5588dad_1         145 KB  conda-forge
    cffi-1.15.0                |  py310hcbf9ad4_0         231 KB  conda-forge
    charset-normalizer-2.0.9   |     pyhd8ed1ab_0          34 KB  conda-forge
    colorama-0.4.4             |     pyh9f0ad1d_0          18 KB  conda-forge
    cryptography-36.0.1        |  py310ha857299_0         1.2 MB  conda-forge
    debugpy-1.5.1              |  py310h8a704f9_0         3.2 MB  conda-forge
    decorator-5.1.0            |     pyhd8ed1ab_0          11 KB  conda-forge
    defusedxml-0.7.1           |     pyhd8ed1ab_0          23 KB  conda-forge
    entrypoints-0.3            |  pyhd8ed1ab_1003           8 KB  conda-forge
    idna-3.1                   |     pyhd3deb0d_0          52 KB  conda-forge
    importlib-metadata-4.10.0  |  py310h5588dad_0          33 KB  conda-forge
    importlib_resources-5.4.0  |     pyhd8ed1ab_0          21 KB  conda-forge
    ipykernel-6.6.0            |  py310hbbfc1a7_0         180 KB  conda-forge
    ipython-7.30.1             |  py310h5588dad_0         1.2 MB  conda-forge
    ipython_genutils-0.2.0     |             py_1          21 KB  conda-forge
    jedi-0.18.1                |  py310h5588dad_0        1004 KB  conda-forge
    jinja2-3.0.3               |     pyhd8ed1ab_0          99 KB  conda-forge
    json5-0.9.5                |     pyh9f0ad1d_0          20 KB  conda-forge
    jsonschema-4.3.2           |     pyhd8ed1ab_0          56 KB  conda-forge
    jupyter_client-7.1.0       |     pyhd8ed1ab_0          89 KB  conda-forge
    jupyter_core-4.9.1         |  py310h5588dad_1         105 KB  conda-forge
    jupyter_server-1.13.1      |     pyhd8ed1ab_0         266 KB  conda-forge
    jupyterlab-3.2.5           |     pyhd8ed1ab_0         5.8 MB  conda-forge
    jupyterlab_pygments-0.1.2  |     pyh9f0ad1d_0           8 KB  conda-forge
    jupyterlab_server-2.10.1   |     pyhd8ed1ab_0          48 KB  conda-forge
    libsodium-1.0.18           |       h8d14728_1         697 KB  conda-forge
    markupsafe-2.0.1           |  py310he2412df_1          25 KB  conda-forge
    matplotlib-inline-0.1.3    |     pyhd8ed1ab_0          11 KB  conda-forge
    mistune-0.8.4              |py310he2412df_1005          55 KB  conda-forge
    nbclassic-0.3.4            |     pyhd8ed1ab_0          22 KB  conda-forge
    nbclient-0.5.9             |     pyhd8ed1ab_0          63 KB  conda-forge
    nbconvert-6.3.0            |  py310h5588dad_1         631 KB  conda-forge
    nbformat-5.1.3             |     pyhd8ed1ab_0          47 KB  conda-forge
    nest-asyncio-1.5.4         |     pyhd8ed1ab_0           9 KB  conda-forge
    notebook-6.4.6             |     pyha770c72_0         6.2 MB  conda-forge
    openssl-1.1.1l             |       h8ffe710_0         5.7 MB  conda-forge
    packaging-21.3             |     pyhd8ed1ab_0          36 KB  conda-forge
    pandoc-2.16.2              |       h8ffe710_0        17.9 MB  conda-forge
    pandocfilters-1.5.0        |     pyhd8ed1ab_0          11 KB  conda-forge
    parso-0.8.3                |     pyhd8ed1ab_0          69 KB  conda-forge
    pickleshare-0.7.5          |          py_1003           9 KB  conda-forge
    prometheus_client-0.12.0   |     pyhd8ed1ab_0          47 KB  conda-forge
    prompt-toolkit-3.0.24      |     pyha770c72_0         249 KB  conda-forge
    pycparser-2.21             |     pyhd8ed1ab_0         100 KB  conda-forge
    pygments-2.10.0            |     pyhd8ed1ab_0         760 KB  conda-forge
    pyopenssl-21.0.0           |     pyhd8ed1ab_0          48 KB  conda-forge
    pyparsing-3.0.6            |     pyhd8ed1ab_0          79 KB  conda-forge
    pyrsistent-0.18.0          |  py310he2412df_0          87 KB  conda-forge
    pysocks-1.7.1              |  py310h5588dad_4          28 KB  conda-forge
    python-dateutil-2.8.2      |     pyhd8ed1ab_0         240 KB  conda-forge
    python_abi-3.10            |          2_cp310           4 KB  conda-forge
    pytz-2021.3                |     pyhd8ed1ab_0         242 KB  conda-forge
    pywin32-302                |  py310he2412df_2         6.9 MB  conda-forge
    pywinpty-1.1.6             |  py310h00ffb61_0         181 KB  conda-forge
    pyzmq-22.3.0               |  py310h73ada01_1         471 KB  conda-forge
    requests-2.26.0            |     pyhd8ed1ab_1          52 KB  conda-forge
    send2trash-1.8.0           |     pyhd8ed1ab_0          17 KB  conda-forge
    six-1.16.0                 |     pyh6c4a22f_0          14 KB  conda-forge
    sniffio-1.2.0              |  py310h5588dad_2          16 KB  conda-forge
    terminado-0.12.1           |  py310h5588dad_1          28 KB  conda-forge
    testpath-0.5.0             |     pyhd8ed1ab_0          86 KB  conda-forge
    tornado-6.1                |  py310he2412df_2         656 KB  conda-forge
    traitlets-5.1.1            |     pyhd8ed1ab_0          82 KB  conda-forge
    ucrt-10.0.20348.0          |       h57928b3_0         1.2 MB  conda-forge
    urllib3-1.26.7             |     pyhd8ed1ab_0         100 KB  conda-forge
    vs2015_runtime-14.29.30037 |       h902a5da_5         1.3 MB  conda-forge
    wcwidth-0.2.5              |     pyh9f0ad1d_2          33 KB  conda-forge
    webencodings-0.5.1         |             py_1          12 KB  conda-forge
    websocket-client-1.2.3     |     pyhd8ed1ab_0          41 KB  conda-forge
    win_inet_pton-1.1.0        |  py310h5588dad_3           9 KB  conda-forge
    winpty-0.4.3               |                4         1.1 MB  conda-forge
    zeromq-4.3.4               |       h0e60522_1         8.9 MB  conda-forge
    zipp-3.6.0                 |     pyhd8ed1ab_0          12 KB  conda-forge
    ------------------------------------------------------------
                                           Total:        75.4 MB

The following NEW packages will be INSTALLED:

  anyio              conda-forge/win-64::anyio-3.4.0-py310h5588dad_0
  argon2-cffi        conda-forge/win-64::argon2-cffi-21.1.0-py310he2412df_2
  async_generator    conda-forge/noarch::async_generator-1.10-py_0
  attrs              conda-forge/noarch::attrs-21.2.0-pyhd8ed1ab_0
  babel              conda-forge/noarch::babel-2.9.1-pyh44b312d_0
  backcall           conda-forge/noarch::backcall-0.2.0-pyh9f0ad1d_0
  backports          conda-forge/noarch::backports-1.0-py_2
  backports.functoo~ conda-forge/noarch::backports.functools_lru_cache-1.6.4-pyhd8ed1ab_0
  bleach             conda-forge/noarch::bleach-4.1.0-pyhd8ed1ab_0
  brotlipy           conda-forge/win-64::brotlipy-0.7.0-py310he2412df_1003
  cffi               conda-forge/win-64::cffi-1.15.0-py310hcbf9ad4_0
  charset-normalizer conda-forge/noarch::charset-normalizer-2.0.9-pyhd8ed1ab_0
  colorama           conda-forge/noarch::colorama-0.4.4-pyh9f0ad1d_0
  cryptography       conda-forge/win-64::cryptography-36.0.1-py310ha857299_0
  debugpy            conda-forge/win-64::debugpy-1.5.1-py310h8a704f9_0
  decorator          conda-forge/noarch::decorator-5.1.0-pyhd8ed1ab_0
  defusedxml         conda-forge/noarch::defusedxml-0.7.1-pyhd8ed1ab_0
  entrypoints        conda-forge/noarch::entrypoints-0.3-pyhd8ed1ab_1003
  idna               conda-forge/noarch::idna-3.1-pyhd3deb0d_0
  importlib-metadata conda-forge/win-64::importlib-metadata-4.10.0-py310h5588dad_0
  importlib_resourc~ conda-forge/noarch::importlib_resources-5.4.0-pyhd8ed1ab_0
  ipykernel          conda-forge/win-64::ipykernel-6.6.0-py310hbbfc1a7_0
  ipython            conda-forge/win-64::ipython-7.30.1-py310h5588dad_0
  ipython_genutils   conda-forge/noarch::ipython_genutils-0.2.0-py_1
  jedi               conda-forge/win-64::jedi-0.18.1-py310h5588dad_0
  jinja2             conda-forge/noarch::jinja2-3.0.3-pyhd8ed1ab_0
  json5              conda-forge/noarch::json5-0.9.5-pyh9f0ad1d_0
  jsonschema         conda-forge/noarch::jsonschema-4.3.2-pyhd8ed1ab_0
  jupyter_client     conda-forge/noarch::jupyter_client-7.1.0-pyhd8ed1ab_0
  jupyter_core       conda-forge/win-64::jupyter_core-4.9.1-py310h5588dad_1
  jupyter_server     conda-forge/noarch::jupyter_server-1.13.1-pyhd8ed1ab_0
  jupyterlab         conda-forge/noarch::jupyterlab-3.2.5-pyhd8ed1ab_0
  jupyterlab_pygmen~ conda-forge/noarch::jupyterlab_pygments-0.1.2-pyh9f0ad1d_0
  jupyterlab_server  conda-forge/noarch::jupyterlab_server-2.10.1-pyhd8ed1ab_0
  libsodium          conda-forge/win-64::libsodium-1.0.18-h8d14728_1
  markupsafe         conda-forge/win-64::markupsafe-2.0.1-py310he2412df_1
  matplotlib-inline  conda-forge/noarch::matplotlib-inline-0.1.3-pyhd8ed1ab_0
  mistune            conda-forge/win-64::mistune-0.8.4-py310he2412df_1005
  nbclassic          conda-forge/noarch::nbclassic-0.3.4-pyhd8ed1ab_0
  nbclient           conda-forge/noarch::nbclient-0.5.9-pyhd8ed1ab_0
  nbconvert          conda-forge/win-64::nbconvert-6.3.0-py310h5588dad_1
  nbformat           conda-forge/noarch::nbformat-5.1.3-pyhd8ed1ab_0
  nest-asyncio       conda-forge/noarch::nest-asyncio-1.5.4-pyhd8ed1ab_0
  notebook           conda-forge/noarch::notebook-6.4.6-pyha770c72_0
  packaging          conda-forge/noarch::packaging-21.3-pyhd8ed1ab_0
  pandoc             conda-forge/win-64::pandoc-2.16.2-h8ffe710_0
  pandocfilters      conda-forge/noarch::pandocfilters-1.5.0-pyhd8ed1ab_0
  parso              conda-forge/noarch::parso-0.8.3-pyhd8ed1ab_0
  pickleshare        conda-forge/noarch::pickleshare-0.7.5-py_1003
  prometheus_client  conda-forge/noarch::prometheus_client-0.12.0-pyhd8ed1ab_0
  prompt-toolkit     conda-forge/noarch::prompt-toolkit-3.0.24-pyha770c72_0
  pycparser          conda-forge/noarch::pycparser-2.21-pyhd8ed1ab_0
  pygments           conda-forge/noarch::pygments-2.10.0-pyhd8ed1ab_0
  pyopenssl          conda-forge/noarch::pyopenssl-21.0.0-pyhd8ed1ab_0
  pyparsing          conda-forge/noarch::pyparsing-3.0.6-pyhd8ed1ab_0
  pyrsistent         conda-forge/win-64::pyrsistent-0.18.0-py310he2412df_0
  pysocks            conda-forge/win-64::pysocks-1.7.1-py310h5588dad_4
  python-dateutil    conda-forge/noarch::python-dateutil-2.8.2-pyhd8ed1ab_0
  python_abi         conda-forge/win-64::python_abi-3.10-2_cp310
  pytz               conda-forge/noarch::pytz-2021.3-pyhd8ed1ab_0
  pywin32            conda-forge/win-64::pywin32-302-py310he2412df_2
  pywinpty           conda-forge/win-64::pywinpty-1.1.6-py310h00ffb61_0
  pyzmq              conda-forge/win-64::pyzmq-22.3.0-py310h73ada01_1
  requests           conda-forge/noarch::requests-2.26.0-pyhd8ed1ab_1
  send2trash         conda-forge/noarch::send2trash-1.8.0-pyhd8ed1ab_0
  six                conda-forge/noarch::six-1.16.0-pyh6c4a22f_0
  sniffio            conda-forge/win-64::sniffio-1.2.0-py310h5588dad_2
  terminado          conda-forge/win-64::terminado-0.12.1-py310h5588dad_1
  testpath           conda-forge/noarch::testpath-0.5.0-pyhd8ed1ab_0
  tornado            conda-forge/win-64::tornado-6.1-py310he2412df_2
  traitlets          conda-forge/noarch::traitlets-5.1.1-pyhd8ed1ab_0
  ucrt               conda-forge/win-64::ucrt-10.0.20348.0-h57928b3_0
  urllib3            conda-forge/noarch::urllib3-1.26.7-pyhd8ed1ab_0
  wcwidth            conda-forge/noarch::wcwidth-0.2.5-pyh9f0ad1d_2
  webencodings       conda-forge/noarch::webencodings-0.5.1-py_1
  websocket-client   conda-forge/noarch::websocket-client-1.2.3-pyhd8ed1ab_0
  win_inet_pton      conda-forge/win-64::win_inet_pton-1.1.0-py310h5588dad_3
  winpty             conda-forge/win-64::winpty-0.4.3-4
  zeromq             conda-forge/win-64::zeromq-4.3.4-h0e60522_1
  zipp               conda-forge/noarch::zipp-3.6.0-pyhd8ed1ab_0

The following packages will be UPDATED:

  certifi            pkgs/main/noarch::certifi-2020.6.20-p~ --> conda-forge/win-64::certifi-2021.10.8-py310h5588dad_1
  vs2015_runtime     pkgs/main::vs2015_runtime-14.27.29016~ --> conda-forge::vs2015_runtime-14.29.30037-h902a5da_5

The following packages will be SUPERSEDED by a higher-priority channel:

  ca-certificates    pkgs/main::ca-certificates-2021.10.26~ --> conda-forge::ca-certificates-2021.10.8-h5b45459_0
  openssl              pkgs/main::openssl-1.1.1l-h2bbff1b_0 --> conda-forge::openssl-1.1.1l-h8ffe710_0


Proceed ([y]/n)? Y


Downloading and Extracting Packages
debugpy-1.5.1        | 3.2 MB    | ############################################################################ | 100%
terminado-0.12.1     | 28 KB     | ############################################################################ | 100%
sniffio-1.2.0        | 16 KB     | ############################################################################ | 100%
importlib-metadata-4 | 33 KB     | ############################################################################ | 100%
async_generator-1.10 | 18 KB     | ############################################################################ | 100%
testpath-0.5.0       | 86 KB     | ############################################################################ | 100%
defusedxml-0.7.1     | 23 KB     | ############################################################################ | 100%
pickleshare-0.7.5    | 9 KB      | ############################################################################ | 100%
pyzmq-22.3.0         | 471 KB    | ############################################################################ | 100%
pandoc-2.16.2        | 17.9 MB   | ############################################################################ | 100%
pywinpty-1.1.6       | 181 KB    | ############################################################################ | 100%
babel-2.9.1          | 6.2 MB    | ############################################################################ | 100%
pygments-2.10.0      | 760 KB    | ############################################################################ | 100%
ucrt-10.0.20348.0    | 1.2 MB    | ############################################################################ | 100%
webencodings-0.5.1   | 12 KB     | ############################################################################ | 100%
attrs-21.2.0         | 44 KB     | ############################################################################ | 100%
pyopenssl-21.0.0     | 48 KB     | ############################################################################ | 100%
pyrsistent-0.18.0    | 87 KB     | ############################################################################ | 100%
ipython_genutils-0.2 | 21 KB     | ############################################################################ | 100%
jinja2-3.0.3         | 99 KB     | ############################################################################ | 100%
nest-asyncio-1.5.4   | 9 KB      | ############################################################################ | 100%
bleach-4.1.0         | 121 KB    | ############################################################################ | 100%
jupyter_core-4.9.1   | 105 KB    | ############################################################################ | 100%
argon2-cffi-21.1.0   | 50 KB     | ############################################################################ | 100%
openssl-1.1.1l       | 5.7 MB    | ############################################################################ | 100%
parso-0.8.3          | 69 KB     | ############################################################################ | 100%
prometheus_client-0. | 47 KB     | ############################################################################ | 100%
backcall-0.2.0       | 13 KB     | ############################################################################ | 100%
pysocks-1.7.1        | 28 KB     | ############################################################################ | 100%
cryptography-36.0.1  | 1.2 MB    | ############################################################################ | 100%
ipykernel-6.6.0      | 180 KB    | ############################################################################ | 100%
libsodium-1.0.18     | 697 KB    | ############################################################################ | 100%
jupyterlab_pygments- | 8 KB      | ############################################################################ | 100%
matplotlib-inline-0. | 11 KB     | ############################################################################ | 100%
python-dateutil-2.8. | 240 KB    | ############################################################################ | 100%
jupyterlab-3.2.5     | 5.8 MB    | ############################################################################ | 100%
prompt-toolkit-3.0.2 | 249 KB    | ############################################################################ | 100%
urllib3-1.26.7       | 100 KB    | ############################################################################ | 100%
jupyter_server-1.13. | 266 KB    | ############################################################################ | 100%
backports.functools_ | 9 KB      | ############################################################################ | 100%
certifi-2021.10.8    | 145 KB    | ############################################################################ | 100%
brotlipy-0.7.0       | 370 KB    | ############################################################################ | 100%
pandocfilters-1.5.0  | 11 KB     | ############################################################################ | 100%
traitlets-5.1.1      | 82 KB     | ############################################################################ | 100%
zipp-3.6.0           | 12 KB     | ############################################################################ | 100%
cffi-1.15.0          | 231 KB    | ############################################################################ | 100%
nbconvert-6.3.0      | 631 KB    | ############################################################################ | 100%
winpty-0.4.3         | 1.1 MB    | ############################################################################ | 100%
decorator-5.1.0      | 11 KB     | ############################################################################ | 100%
jupyterlab_server-2. | 48 KB     | ############################################################################ | 100%
pywin32-302          | 6.9 MB    | ############################################################################ | 100%
ca-certificates-2021 | 176 KB    | ############################################################################ | 100%
anyio-3.4.0          | 154 KB    | ############################################################################ | 100%
jsonschema-4.3.2     | 56 KB     | ############################################################################ | 100%
colorama-0.4.4       | 18 KB     | ############################################################################ | 100%
ipython-7.30.1       | 1.2 MB    | ############################################################################ | 100%
requests-2.26.0      | 52 KB     | ############################################################################ | 100%
zeromq-4.3.4         | 8.9 MB    | ############################################################################ | 100%
notebook-6.4.6       | 6.2 MB    | ############################################################################ | 100%
backports-1.0        | 4 KB      | ############################################################################ | 100%
win_inet_pton-1.1.0  | 9 KB      | ############################################################################ | 100%
nbclient-0.5.9       | 63 KB     | ############################################################################ | 100%
wcwidth-0.2.5        | 33 KB     | ############################################################################ | 100%
importlib_resources- | 21 KB     | ############################################################################ | 100%
nbclassic-0.3.4      | 22 KB     | ############################################################################ | 100%
vs2015_runtime-14.29 | 1.3 MB    | ############################################################################ | 100%
pyparsing-3.0.6      | 79 KB     | ############################################################################ | 100%
mistune-0.8.4        | 55 KB     | ############################################################################ | 100%
tornado-6.1          | 656 KB    | ############################################################################ | 100%
python_abi-3.10      | 4 KB      | ############################################################################ | 100%
pytz-2021.3          | 242 KB    | ############################################################################ | 100%
json5-0.9.5          | 20 KB     | ############################################################################ | 100%
six-1.16.0           | 14 KB     | ############################################################################ | 100%
markupsafe-2.0.1     | 25 KB     | ############################################################################ | 100%
send2trash-1.8.0     | 17 KB     | ############################################################################ | 100%
websocket-client-1.2 | 41 KB     | ############################################################################ | 100%
jupyter_client-7.1.0 | 89 KB     | ############################################################################ | 100%
packaging-21.3       | 36 KB     | ############################################################################ | 100%
charset-normalizer-2 | 34 KB     | ############################################################################ | 100%
nbformat-5.1.3       | 47 KB     | ############################################################################ | 100%
entrypoints-0.3      | 8 KB      | ############################################################################ | 100%
jedi-0.18.1          | 1004 KB   | ############################################################################ | 100%
pycparser-2.21       | 100 KB    | ############################################################################ | 100%
idna-3.1             | 52 KB     | ############################################################################ | 100%
Preparing transaction: done
Verifying transaction: done
Executing transaction: done
```

### npm install -g tslab

#### reference
- https://github.com/yunabe/tslab
- https://dev.classmethod.jp/articles/ts-action/


#### installation logs
```cmd

(jup) G:\workspace\jupnote>npm install -g tslab

G:\workspace\jupnote>tslab install --version
tslab 1.0.15

G:\workspace\jupnote>tslab install
Running python C:\Users\sakai\AppData\Roaming\npm\node_modules\tslab\python\install.py --tslab=tslab.cmd
jupyter is not installed in this Python.

G:\workspace\jupnote>conda activate jup

(jup) G:\workspace\jupnote>tslab install
Running python C:\Users\sakai\AppData\Roaming\npm\node_modules\tslab\python\install.py --tslab=tslab.cmd
Installing TypeScript kernel spec
Installing JavaScript kernel spec

(jup) G:\workspace\jupnote>jupyter kernelspec list
Available kernels:
  jslab      C:\Users\sakai\AppData\Roaming\jupyter\kernels\jslab
  python3    C:\Users\sakai\AppData\Roaming\jupyter\kernels\python3
  tslab      C:\Users\sakai\AppData\Roaming\jupyter\kernels\tslab
```

## pip install powershell_kernel

### reference
- https://github.com/vors/jupyter-powershell
- https://devblogs.microsoft.com/powershell/public-preview-of-powershell-support-in-jupyter-notebooks/

```cmd
G:\>conda activate jup

(jup) G:\>pip install powershell_kernel
Collecting powershell_kernel
  Downloading powershell_kernel-0.1.4.tar.gz (6.6 kB)
Building wheels for collected packages: powershell-kernel
  Building wheel for powershell-kernel (setup.py) ... done
  Created wheel for powershell-kernel: filename=powershell_kernel-0.1.4-py3-none-any.whl size=7921 sha256=c791427c3172d438713690b6fdafbf8e400a57e1901f65c43b198760855d4366
  Stored in directory: c:\users\sakai\appdata\local\pip\cache\wheels\f0\9d\b5\e891804aa76636f56598460c22a2d2c76be3d37098afede4cd
Successfully built powershell-kernel
Installing collected packages: powershell-kernel
Successfully installed powershell-kernel-0.1.4

(jup) G:\>python -m powershell_kernel.install
Using powershell_command='powershell'
Installing IPython kernel spec

(jup) G:\>jupyter kernelspec list
Available kernels:
  jslab         C:\Users\sakai\AppData\Roaming\jupyter\kernels\jslab
  powershell    C:\Users\sakai\AppData\Roaming\jupyter\kernels\powershell
  python3       C:\Users\sakai\AppData\Roaming\jupyter\kernels\python3
  tslab         C:\Users\sakai\AppData\Roaming\jupyter\kernels\tslab

(jup) G:\>
```


