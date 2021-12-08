---
title: "2112-miniconda-setting"
emoji: "🐍"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["conda"]
published: false
reviewed: false
---
# 2112-conda-setting

## overview
- Set miniconda, that is a free minimal installer for conda. It is a small, bootstrap version of Anaconda that includes only conda, python, the package they depend on, and a small number of other useful packages, including pip, zlib and a few others. Use the `conda install` command to install 720+ additional packages from Anaconda repository.

## reference
- https://docs.conda.io/en/latest/miniconda.html

## download
![screanshot](https://gyazo.com/404b6006f3f55eb5d838445eec6b3df4.png)

## installation
- install with download exe.

## environment
- path 
```
PS C:\Users\sakai> $Env:path -split ";"  | oss | sls "conda"

C:\Users\sakai\miniconda3
C:\Users\sakai\miniconda3\Library\mingw-w64\bin
C:\Users\sakai\miniconda3\Library\usr\bin
C:\Users\sakai\miniconda3\Library\bin
C:\Users\sakai\miniconda3\Scripts

```
- confirm the installation
```
PS C:\Users\sakai> conda --version
conda 4.10.3
PS C:\Users\sakai> conda --help
usage: conda-script.py [-h] [-V] command ...

conda is a tool for managing and deploying applications, environments and packages.

Options:

positional arguments:
  command
    clean        Remove unused packages and caches.
    compare      Compare packages between conda environments.
    config       Modify configuration values in .condarc. This is modeled after the git config command. Writes to the
                 user .condarc file (C:\Users\sakai\.condarc) by default.
    create       Create a new conda environment from a list of specified packages.
    help         Displays a list of available conda commands and their help strings.
    info         Display information about current conda install.
    init         Initialize conda for shell interaction. [Experimental]
    install      Installs a list of packages into a specified conda environment.
    list         List linked packages in a conda environment.
    package      Low-level conda package utility. (EXPERIMENTAL)
    remove       Remove a list of packages from a specified conda environment.
    uninstall    Alias for conda remove.
    run          Run an executable in a conda environment. [Experimental]
    search       Search for packages and display associated information. The input is a MatchSpec, a query language
                 for conda packages. See examples below.
    update       Updates conda packages to the latest compatible version.
    upgrade      Alias for conda update.

optional arguments:
  -h, --help     Show this help message and exit.
  -V, --version  Show the conda version number and exit.

conda commands available from other packages:
  env
```

### conda list
```
PS C:\Users\sakai> conda list
# packages in environment at C:\Users\sakai\miniconda3:
#
# Name                    Version                   Build  Channel
brotlipy                  0.7.0           py39h2bbff1b_1003
ca-certificates           2021.7.5             haa95532_1
certifi                   2021.5.30        py39haa95532_0
cffi                      1.14.6           py39h2bbff1b_0
chardet                   4.0.0           py39haa95532_1003
conda                     4.10.3           py39haa95532_0
conda-package-handling    1.7.3            py39h8cc25b3_1
console_shortcut          0.1.1                         4
cryptography              3.4.7            py39h71e12ea_0
idna                      2.10               pyhd3eb1b0_0
menuinst                  1.4.16           py39h2bbff1b_0
openssl                   1.1.1k               h2bbff1b_0
pip                       21.1.3           py39haa95532_0
powershell_shortcut       0.0.1                         3
pycosat                   0.6.3            py39h2bbff1b_0
pycparser                 2.20                       py_2
pyopenssl                 20.0.1             pyhd3eb1b0_1
pysocks                   1.7.1            py39haa95532_0
python                    3.9.5                h6244533_3
pywin32                   228              py39he774522_0
requests                  2.25.1             pyhd3eb1b0_0
ruamel_yaml               0.15.100         py39h2bbff1b_0
setuptools                52.0.0           py39haa95532_0
six                       1.16.0             pyhd3eb1b0_0
sqlite                    3.36.0               h2bbff1b_0
tqdm                      4.61.2             pyhd3eb1b0_1
tzdata                    2021a                h52ac0ba_0
urllib3                   1.26.6             pyhd3eb1b0_1
vc                        14.2                 h21ff451_1
vs2015_runtime            14.27.29016          h5e58377_2
wheel                     0.36.2             pyhd3eb1b0_0
win_inet_pton             1.1.0            py39haa95532_0
wincertstore              0.2              py39h2bbff1b_0
yaml                      0.2.5                he774522_0
PS C:\Users\sakai>
```

## conda create -n jup pip python

- jupyter notebookをインストールするための環境構築

```
PS G:\> conda --version
conda 4.10.3
PS G:\> conda create -n jup pip python
Collecting package metadata (current_repodata.json): done
Solving environment: done

## Package Plan ##

  environment location: C:\Users\sakai\miniconda3\envs\jup

  added / updated specs:
    - pip
    - python


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    bzip2-1.0.8                |       he774522_0         113 KB
    ca-certificates-2021.10.26 |       haa95532_2         115 KB
    certifi-2020.6.20          |     pyhd3eb1b0_3         155 KB
    libffi-3.4.2               |       h604cdb4_1          43 KB
    openssl-1.1.1l             |       h2bbff1b_0         4.8 MB
    pip-21.2.4                 |  py310haa95532_0         1.9 MB
    python-3.10.0              |       h96c0403_3        13.0 MB
    setuptools-58.0.4          |  py310haa95532_0         784 KB
    tk-8.6.11                  |       h2bbff1b_0         3.3 MB
    tzdata-2021e               |       hda174b7_0         112 KB
    wheel-0.37.0               |     pyhd3eb1b0_1          33 KB
    wincertstore-0.2           |  py310haa95532_2          15 KB
    xz-5.2.5                   |       h62dcd97_0         244 KB
    zlib-1.2.11                |       h62dcd97_4         113 KB
    ------------------------------------------------------------
                                           Total:        24.6 MB

The following NEW packages will be INSTALLED:

  bzip2              pkgs/main/win-64::bzip2-1.0.8-he774522_0
  ca-certificates    pkgs/main/win-64::ca-certificates-2021.10.26-haa95532_2
  certifi            pkgs/main/noarch::certifi-2020.6.20-pyhd3eb1b0_3
  libffi             pkgs/main/win-64::libffi-3.4.2-h604cdb4_1
  openssl            pkgs/main/win-64::openssl-1.1.1l-h2bbff1b_0
  pip                pkgs/main/win-64::pip-21.2.4-py310haa95532_0
  python             pkgs/main/win-64::python-3.10.0-h96c0403_3
  setuptools         pkgs/main/win-64::setuptools-58.0.4-py310haa95532_0
  sqlite             pkgs/main/win-64::sqlite-3.36.0-h2bbff1b_0
  tk                 pkgs/main/win-64::tk-8.6.11-h2bbff1b_0
  tzdata             pkgs/main/noarch::tzdata-2021e-hda174b7_0
  vc                 pkgs/main/win-64::vc-14.2-h21ff451_1
  vs2015_runtime     pkgs/main/win-64::vs2015_runtime-14.27.29016-h5e58377_2
  wheel              pkgs/main/noarch::wheel-0.37.0-pyhd3eb1b0_1
  wincertstore       pkgs/main/win-64::wincertstore-0.2-py310haa95532_2
  xz                 pkgs/main/win-64::xz-5.2.5-h62dcd97_0
  zlib               pkgs/main/win-64::zlib-1.2.11-h62dcd97_4


Proceed ([y]/n)? y


Downloading and Extracting Packages
bzip2-1.0.8          | 113 KB    | ############################################################################ | 100%
wheel-0.37.0         | 33 KB     | ############################################################################ | 100%
libffi-3.4.2         | 43 KB     | ############################################################################ | 100%
tzdata-2021e         | 112 KB    | ############################################################################ | 100%
pip-21.2.4           | 1.9 MB    | ############################################################################ | 100%
ca-certificates-2021 | 115 KB    | ############################################################################ | 100%
certifi-2020.6.20    | 155 KB    | ############################################################################ | 100%
zlib-1.2.11          | 113 KB    | ############################################################################ | 100%
python-3.10.0        | 13.0 MB   | ############################################################################ | 100%
wincertstore-0.2     | 15 KB     | ############################################################################ | 100%
setuptools-58.0.4    | 784 KB    | ############################################################################ | 100%
xz-5.2.5             | 244 KB    | ############################################################################ | 100%
tk-8.6.11            | 3.3 MB    | ############################################################################ | 100%
openssl-1.1.1l       | 4.8 MB    | ############################################################################ | 100%
Preparing transaction: done
Verifying transaction: done
Executing transaction: done
#
# To activate this environment, use
#
#     $ conda activate jup
#
# To deactivate an active environment, use
#
#     $ conda deactivate
```

- conda env list / conda activate jup

```
PS G:\> conda env list
# conda environments:
#
base                  *  C:\Users\sakai\miniconda3
jup                      C:\Users\sakai\miniconda3\envs\jup

PS G:\> conda activate jup
```

### conda console
```
(base) PS C:\Users\sakai> conda env list
# conda environments:
#
base                  *  C:\Users\sakai\miniconda3
jup                      C:\Users\sakai\miniconda3\envs\jup

(base) PS C:\Users\sakai> conda activate jup
(jup) PS C:\Users\sakai>

```

## reference for conda command of managing environment
- https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html
- https://starpentagon.net/analytics/conda_env_jupyter_notebook/


## set ipykernel
```
(base) PS C:\Users\sakai> activate jup
(base) PS C:\Users\sakai> conda activate jup
(jup) PS C:\Users\sakai> conda install notebook ipykernel
Collecting package metadata (current_repodata.json): done
Solving environment: failed with initial frozen solve. Retrying with flexible solve.
Collecting package metadata (repodata.json): done
Solving environment: failed with initial frozen solve. Retrying with flexible solve.

PackagesNotFoundError: The following packages are not available from current channels:

  - python=3.1

Current channels:

  - https://repo.anaconda.com/pkgs/main/win-64
  - https://repo.anaconda.com/pkgs/main/noarch
  - https://repo.anaconda.com/pkgs/r/win-64
  - https://repo.anaconda.com/pkgs/r/noarch
  - https://repo.anaconda.com/pkgs/msys2/win-64
  - https://repo.anaconda.com/pkgs/msys2/noarch

To search for alternate channels that may provide the conda package you're
looking for, navigate to

    https://anaconda.org

and use the search bar at the top of the page.


(jup) PS C:\Users\sakai> ipython kernel install --user --display-name jup
Installed kernelspec python3 in C:\Users\sakai\AppData\Roaming\jupyter\kernels\python3
(jup) PS C:\Users\sakai> jupyter notebook
[I 17:51:11.613 NotebookApp] The port 8888 is already in use, trying another port.
[I 17:51:11.620 NotebookApp] Serving notebooks from local directory: C:\Users\sakai
[I 17:51:11.621 NotebookApp] Jupyter Notebook 6.4.6 is running at:
[I 17:51:11.621 NotebookApp] http://localhost:8889/?token=7dc92e445f892f1cf17122e38bd8d32e59b709e96976298a
[I 17:51:11.621 NotebookApp]  or http://127.0.0.1:8889/?token=7dc92e445f892f1cf17122e38bd8d32e59b709e96976298a
[I 17:51:11.622 NotebookApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
[C 17:51:12.057 NotebookApp]

    To access the notebook, open this file in a browser:
        file:///C:/Users/sakai/AppData/Roaming/jupyter/runtime/nbserver-7220-open.html
    Or copy and paste one of these URLs:
        http://localhost:8889/?token=7dc92e445f892f1cf17122e38bd8d32e59b709e96976298a
     or http://127.0.0.1:8889/?token=7dc92e445f892f1cf17122e38bd8d32e59b709e96976298a

```

## Powershell support in Jupyter Notebook

### reference
- https://devblogs.microsoft.com/powershell/public-preview-of-powershell-support-in-jupyter-notebooks/

## TypeScript support in Jupyter Notebook
- https://stackoverflow.com/questions/55080181/typescript-in-jupyter-notebook
- https://dev.classmethod.jp/articles/ts-action/


[end of file]