# jupyter note


## install

### 2019/05/14

```
$ brew install miniconda
```

を実行した。

### 2019/05/16

.zshrc を編集、パスを通す。

```
# miniconda
PATH=/usr/local/miniconda3/bin/:$PATH
```

```
$ conda list
# packages in environment at /usr/local/miniconda3:
#
# Name                    Version                   Build  Channel
asn1crypto                0.24.0                   py37_0
ca-certificates           2018.03.07                    0
certifi                   2018.11.29               py37_0
cffi                      1.11.5           py37h6174b99_1
chardet                   3.0.4                    py37_1
conda                     4.5.12                   py37_0
conda-env                 2.6.0                         1
cryptography              2.4.2            py37ha12b0ac_0
idna                      2.8                      py37_0
libcxx                    4.0.1                hcfea43d_1
libcxxabi                 4.0.1                hcfea43d_1
libedit                   3.1.20170329         hb402a30_2
libffi                    3.2.1                h475c297_4
ncurses                   6.1                  h0a44026_1
openssl                   1.1.1a               h1de35cc_0
pip                       18.1                     py37_0
pycosat                   0.6.3            py37h1de35cc_0
pycparser                 2.19                     py37_0
pyopenssl                 18.0.0                   py37_0
pysocks                   1.6.8                    py37_0
python                    3.7.1                haf84260_7
python.app                2                        py37_9
readline                  7.0                  h1de35cc_5
requests                  2.21.0                   py37_0
ruamel_yaml               0.15.46          py37h1de35cc_0
setuptools                40.6.3                   py37_0
six                       1.12.0                   py37_0
sqlite                    3.26.0               ha441bb4_0
tk                        8.6.8                ha441bb4_0
urllib3                   1.24.1                   py37_0
wheel                     0.32.3                   py37_0
xz                        5.2.4                h1de35cc_4
yaml                      0.1.7                hc338f04_2
zlib                      1.2.11               h1de35cc_3
```


```
$ conda create -n notebook
Solving environment: done


==> WARNING: A newer version of conda exists. <==
  current version: 4.5.12
    latest version: 4.6.14

Please update conda by running

    $ conda update -n base -c defaults conda



## Package Plan ##

  environment location: /usr/local/miniconda3/envs/notebook


Proceed ([y]/n)?

Preparing transaction: done
Verifying transaction: done
Executing transaction: done
#
# To activate this environment, use:
# > source activate notebook
#
# To deactivate an active environment, use:
# > source deactivate
#

conda create -n notebook  4.93s user 0.35s system 12% cpu 42.541 total
```

```
$ conda update -n base -c defaults conda
Solving environment: done

## Package Plan ##

  environment location: /usr/local/miniconda3

  added / updated specs:
    - conda


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    openssl-1.1.1b             |       h1de35cc_1         3.4 MB
    certifi-2019.3.9           |           py37_0         155 KB
    ca-certificates-2019.1.23  |                0         126 KB
    conda-4.6.14               |           py37_0         2.1 MB
    ------------------------------------------------------------
                                           Total:         5.8 MB

The following packages will be UPDATED:

    ca-certificates: 2018.03.07-0      --> 2019.1.23-0
    certifi:         2018.11.29-py37_0 --> 2019.3.9-py37_0
    conda:           4.5.12-py37_0     --> 4.6.14-py37_0
    openssl:         1.1.1a-h1de35cc_0 --> 1.1.1b-h1de35cc_1

Proceed ([y]/n)?


Downloading and Extracting Packages
openssl-1.1.1b       | 3.4 MB    | ####################################################################################################################################### | 100%
certifi-2019.3.9     | 155 KB    | ####################################################################################################################################### | 100%
ca-certificates-2019 | 126 KB    | ####################################################################################################################################### | 100%
conda-4.6.14         | 2.1 MB    | ####################################################################################################################################### | 100%
Preparing transaction: done
Verifying transaction: done
Executing transaction: done
conda update -n base -c defaults conda  5.50s user 2.59s system 23% cpu 33.764 total
```


```
$ conda activate notebook
(notebook) $ conda install numpy pandas matplotlib jupyter
Collecting package metadata: done
Solving environment: done

## Package Plan ##

  environment location: /usr/local/miniconda3/envs/notebook

  added / updated specs:
    - jupyter
    - matplotlib
    - numpy
    - pandas


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    appnope-0.1.0              |           py37_0           8 KB
    attrs-19.1.0               |           py37_1          56 KB
    backcall-0.1.0             |           py37_0          20 KB
    blas-1.0                   |              mkl           5 KB
    bleach-3.1.0               |           py37_0         221 KB
    cycler-0.10.0              |           py37_0          14 KB
    dbus-1.13.6                |       h90a0687_0         560 KB
    decorator-4.4.0            |           py37_1          18 KB
    defusedxml-0.6.0           |             py_0          23 KB
    entrypoints-0.3            |           py37_0          12 KB
    expat-2.2.6                |       h0a44026_0         129 KB
    freetype-2.9.1             |       hb4e5f40_0         864 KB
    gettext-0.19.8.1           |       h15daf44_3         3.4 MB
    glib-2.56.2                |       hd9629dc_0         4.7 MB
    icu-58.2                   |       h4b95b61_1        22.3 MB
    intel-openmp-2019.3        |              199         1.1 MB
    ipykernel-5.1.0            |   py37h39e3cac_0         156 KB
    ipython-7.5.0              |   py37h39e3cac_0         1.1 MB
    ipython_genutils-0.2.0     |           py37_0          39 KB
    ipywidgets-7.4.2           |           py37_0         151 KB
    jedi-0.13.3                |           py37_0         236 KB
    jinja2-2.10.1              |           py37_0         188 KB
    jpeg-9b                    |       he5867d9_2         236 KB
    jsonschema-3.0.1           |           py37_0          88 KB
    jupyter-1.0.0              |           py37_7           6 KB
    jupyter_client-5.2.4       |           py37_0         127 KB
    jupyter_console-6.0.0      |           py37_0          35 KB
    jupyter_core-4.4.0         |           py37_0          63 KB
    kiwisolver-1.1.0           |   py37h0a44026_0          60 KB
    libedit-3.1.20181209       |       hb402a30_0         159 KB
    libgfortran-3.0.1          |       h93005f0_2         495 KB
    libiconv-1.15              |       hdd342a3_7         1.3 MB
    libpng-1.6.37              |       ha441bb4_0         325 KB
    libsodium-1.0.16           |       h3efe00b_0         324 KB
    markupsafe-1.1.1           |   py37h1de35cc_0          28 KB
    matplotlib-3.0.3           |   py37h54f8f79_0         6.6 MB
    mistune-0.8.4              |   py37h1de35cc_0          54 KB
    mkl-2019.3                 |              199       154.7 MB
    mkl_fft-1.0.12             |   py37h5e564d8_0         155 KB
    mkl_random-1.0.2           |   py37h27c97d8_0         358 KB
    nbconvert-5.5.0            |             py_0         381 KB
    nbformat-4.4.0             |           py37_0         141 KB
    notebook-5.7.8             |           py37_0         7.3 MB
    numpy-1.16.3               |   py37hacdab7b_0          49 KB
    numpy-base-1.16.3          |   py37h6575580_0         4.2 MB
    pandas-0.24.2              |   py37h0a44026_0         9.9 MB
    pandoc-2.2.3.2             |                0        13.8 MB
    pandocfilters-1.4.2        |           py37_1          13 KB
    parso-0.4.0                |             py_0          66 KB
    pcre-8.43                  |       h0a44026_0         227 KB
    pexpect-4.7.0              |           py37_0          82 KB
    pickleshare-0.7.5          |           py37_0          12 KB
    pip-19.1.1                 |           py37_0         1.8 MB
    prometheus_client-0.6.0    |           py37_0          69 KB
    prompt_toolkit-2.0.9       |           py37_0         488 KB
    ptyprocess-0.6.0           |           py37_0          23 KB
    pygments-2.4.0             |             py_0         664 KB
    pyparsing-2.4.0            |             py_0          58 KB
    pyqt-5.9.2                 |   py37h655552a_2         4.4 MB
    pyrsistent-0.14.11         |   py37h1de35cc_0          88 KB
    python-3.7.3               |       h359304d_0        21.7 MB
    python-dateutil-2.8.0      |           py37_0         281 KB
    pytz-2019.1                |             py_0         236 KB
    pyzmq-18.0.0               |   py37h0a44026_0         457 KB
    qt-5.9.7                   |       h468cd18_1        76.8 MB
    qtconsole-4.4.4            |             py_0          88 KB
    send2trash-1.5.0           |           py37_0          16 KB
    setuptools-41.0.1          |           py37_0         635 KB
    sip-4.19.8                 |   py37h0a44026_0         252 KB
    sqlite-3.28.0              |       ha441bb4_0         2.3 MB
    terminado-0.8.2            |           py37_0          22 KB
    testpath-0.4.2             |           py37_0          91 KB
    tornado-6.0.2              |   py37h1de35cc_0         642 KB
    traitlets-4.3.2            |           py37_0         133 KB
    wcwidth-0.1.7              |           py37_0          23 KB
    webencodings-0.5.1         |           py37_1          19 KB
    wheel-0.33.4               |           py37_0          39 KB
    widgetsnbextension-3.4.2   |           py37_0         1.7 MB
    zeromq-4.3.1               |       h0a44026_3         565 KB
    ------------------------------------------------------------
                                           Total:       350.0 MB

The following NEW packages will be INSTALLED:

  appnope            pkgs/main/osx-64::appnope-0.1.0-py37_0
  attrs              pkgs/main/osx-64::attrs-19.1.0-py37_1
  backcall           pkgs/main/osx-64::backcall-0.1.0-py37_0
  blas               pkgs/main/osx-64::blas-1.0-mkl
  bleach             pkgs/main/osx-64::bleach-3.1.0-py37_0
  ca-certificates    pkgs/main/osx-64::ca-certificates-2019.1.23-0
  certifi            pkgs/main/osx-64::certifi-2019.3.9-py37_0
  cycler             pkgs/main/osx-64::cycler-0.10.0-py37_0
  dbus               pkgs/main/osx-64::dbus-1.13.6-h90a0687_0
  decorator          pkgs/main/osx-64::decorator-4.4.0-py37_1
  defusedxml         pkgs/main/noarch::defusedxml-0.6.0-py_0
  entrypoints        pkgs/main/osx-64::entrypoints-0.3-py37_0
  expat              pkgs/main/osx-64::expat-2.2.6-h0a44026_0
  freetype           pkgs/main/osx-64::freetype-2.9.1-hb4e5f40_0
  gettext            pkgs/main/osx-64::gettext-0.19.8.1-h15daf44_3
  glib               pkgs/main/osx-64::glib-2.56.2-hd9629dc_0
  icu                pkgs/main/osx-64::icu-58.2-h4b95b61_1
  intel-openmp       pkgs/main/osx-64::intel-openmp-2019.3-199
  ipykernel          pkgs/main/osx-64::ipykernel-5.1.0-py37h39e3cac_0
  ipython            pkgs/main/osx-64::ipython-7.5.0-py37h39e3cac_0
  ipython_genutils   pkgs/main/osx-64::ipython_genutils-0.2.0-py37_0
  ipywidgets         pkgs/main/osx-64::ipywidgets-7.4.2-py37_0
  jedi               pkgs/main/osx-64::jedi-0.13.3-py37_0
  jinja2             pkgs/main/osx-64::jinja2-2.10.1-py37_0
  jpeg               pkgs/main/osx-64::jpeg-9b-he5867d9_2
  jsonschema         pkgs/main/osx-64::jsonschema-3.0.1-py37_0
  jupyter            pkgs/main/osx-64::jupyter-1.0.0-py37_7
  jupyter_client     pkgs/main/osx-64::jupyter_client-5.2.4-py37_0
  jupyter_console    pkgs/main/osx-64::jupyter_console-6.0.0-py37_0
  jupyter_core       pkgs/main/osx-64::jupyter_core-4.4.0-py37_0
  kiwisolver         pkgs/main/osx-64::kiwisolver-1.1.0-py37h0a44026_0
  libcxx             pkgs/main/osx-64::libcxx-4.0.1-hcfea43d_1
  libcxxabi          pkgs/main/osx-64::libcxxabi-4.0.1-hcfea43d_1
  libedit            pkgs/main/osx-64::libedit-3.1.20181209-hb402a30_0
  libffi             pkgs/main/osx-64::libffi-3.2.1-h475c297_4
  libgfortran        pkgs/main/osx-64::libgfortran-3.0.1-h93005f0_2
  libiconv           pkgs/main/osx-64::libiconv-1.15-hdd342a3_7
  libpng             pkgs/main/osx-64::libpng-1.6.37-ha441bb4_0
  libsodium          pkgs/main/osx-64::libsodium-1.0.16-h3efe00b_0
  markupsafe         pkgs/main/osx-64::markupsafe-1.1.1-py37h1de35cc_0
  matplotlib         pkgs/main/osx-64::matplotlib-3.0.3-py37h54f8f79_0
  mistune            pkgs/main/osx-64::mistune-0.8.4-py37h1de35cc_0
  mkl                pkgs/main/osx-64::mkl-2019.3-199
  mkl_fft            pkgs/main/osx-64::mkl_fft-1.0.12-py37h5e564d8_0
  mkl_random         pkgs/main/osx-64::mkl_random-1.0.2-py37h27c97d8_0
  nbconvert          pkgs/main/noarch::nbconvert-5.5.0-py_0
  nbformat           pkgs/main/osx-64::nbformat-4.4.0-py37_0
  ncurses            pkgs/main/osx-64::ncurses-6.1-h0a44026_1
  notebook           pkgs/main/osx-64::notebook-5.7.8-py37_0
  numpy              pkgs/main/osx-64::numpy-1.16.3-py37hacdab7b_0
  numpy-base         pkgs/main/osx-64::numpy-base-1.16.3-py37h6575580_0
  openssl            pkgs/main/osx-64::openssl-1.1.1b-h1de35cc_1
  pandas             pkgs/main/osx-64::pandas-0.24.2-py37h0a44026_0
  pandoc             pkgs/main/osx-64::pandoc-2.2.3.2-0
  pandocfilters      pkgs/main/osx-64::pandocfilters-1.4.2-py37_1
  parso              pkgs/main/noarch::parso-0.4.0-py_0
  pcre               pkgs/main/osx-64::pcre-8.43-h0a44026_0
  pexpect            pkgs/main/osx-64::pexpect-4.7.0-py37_0
  pickleshare        pkgs/main/osx-64::pickleshare-0.7.5-py37_0
  pip                pkgs/main/osx-64::pip-19.1.1-py37_0
  prometheus_client  pkgs/main/osx-64::prometheus_client-0.6.0-py37_0
  prompt_toolkit     pkgs/main/osx-64::prompt_toolkit-2.0.9-py37_0
  ptyprocess         pkgs/main/osx-64::ptyprocess-0.6.0-py37_0
  pygments           pkgs/main/noarch::pygments-2.4.0-py_0
  pyparsing          pkgs/main/noarch::pyparsing-2.4.0-py_0
  pyqt               pkgs/main/osx-64::pyqt-5.9.2-py37h655552a_2
  pyrsistent         pkgs/main/osx-64::pyrsistent-0.14.11-py37h1de35cc_0
  python             pkgs/main/osx-64::python-3.7.3-h359304d_0
  python-dateutil    pkgs/main/osx-64::python-dateutil-2.8.0-py37_0
  pytz               pkgs/main/noarch::pytz-2019.1-py_0
  pyzmq              pkgs/main/osx-64::pyzmq-18.0.0-py37h0a44026_0
  qt                 pkgs/main/osx-64::qt-5.9.7-h468cd18_1
  qtconsole          pkgs/main/noarch::qtconsole-4.4.4-py_0
  readline           pkgs/main/osx-64::readline-7.0-h1de35cc_5
  send2trash         pkgs/main/osx-64::send2trash-1.5.0-py37_0
  setuptools         pkgs/main/osx-64::setuptools-41.0.1-py37_0
  sip                pkgs/main/osx-64::sip-4.19.8-py37h0a44026_0
  six                pkgs/main/osx-64::six-1.12.0-py37_0
  sqlite             pkgs/main/osx-64::sqlite-3.28.0-ha441bb4_0
  terminado          pkgs/main/osx-64::terminado-0.8.2-py37_0
  testpath           pkgs/main/osx-64::testpath-0.4.2-py37_0
  tk                 pkgs/main/osx-64::tk-8.6.8-ha441bb4_0
  tornado            pkgs/main/osx-64::tornado-6.0.2-py37h1de35cc_0
  traitlets          pkgs/main/osx-64::traitlets-4.3.2-py37_0
  wcwidth            pkgs/main/osx-64::wcwidth-0.1.7-py37_0
  webencodings       pkgs/main/osx-64::webencodings-0.5.1-py37_1
  wheel              pkgs/main/osx-64::wheel-0.33.4-py37_0
  widgetsnbextension pkgs/main/osx-64::widgetsnbextension-3.4.2-py37_0
  xz                 pkgs/main/osx-64::xz-5.2.4-h1de35cc_4
  zeromq             pkgs/main/osx-64::zeromq-4.3.1-h0a44026_3
  zlib               pkgs/main/osx-64::zlib-1.2.11-h1de35cc_3


Proceed ([y]/n)? n


CondaSystemExit: Exiting.

  13.59s user 0.45s system 32% cpu 42.642 total
(notebook) $ conda install numpy pandas matplotlib jupyter notebook
Collecting package metadata: done
Solving environment: done

## Package Plan ##

  environment location: /usr/local/miniconda3/envs/notebook

  added / updated specs:
    - jupyter
    - matplotlib
    - notebook
    - numpy
    - pandas


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    appnope-0.1.0              |           py37_0           8 KB
    attrs-19.1.0               |           py37_1          56 KB
    backcall-0.1.0             |           py37_0          20 KB
    blas-1.0                   |              mkl           5 KB
    bleach-3.1.0               |           py37_0         221 KB
    cycler-0.10.0              |           py37_0          14 KB
    dbus-1.13.6                |       h90a0687_0         560 KB
    decorator-4.4.0            |           py37_1          18 KB
    defusedxml-0.6.0           |             py_0          23 KB
    entrypoints-0.3            |           py37_0          12 KB
    expat-2.2.6                |       h0a44026_0         129 KB
    freetype-2.9.1             |       hb4e5f40_0         864 KB
    gettext-0.19.8.1           |       h15daf44_3         3.4 MB
    glib-2.56.2                |       hd9629dc_0         4.7 MB
    icu-58.2                   |       h4b95b61_1        22.3 MB
    intel-openmp-2019.3        |              199         1.1 MB
    ipykernel-5.1.0            |   py37h39e3cac_0         156 KB
    ipython-7.5.0              |   py37h39e3cac_0         1.1 MB
    ipython_genutils-0.2.0     |           py37_0          39 KB
    ipywidgets-7.4.2           |           py37_0         151 KB
    jedi-0.13.3                |           py37_0         236 KB
    jinja2-2.10.1              |           py37_0         188 KB
    jpeg-9b                    |       he5867d9_2         236 KB
    jsonschema-3.0.1           |           py37_0          88 KB
    jupyter-1.0.0              |           py37_7           6 KB
    jupyter_client-5.2.4       |           py37_0         127 KB
    jupyter_console-6.0.0      |           py37_0          35 KB
    jupyter_core-4.4.0         |           py37_0          63 KB
    kiwisolver-1.1.0           |   py37h0a44026_0          60 KB
    libedit-3.1.20181209       |       hb402a30_0         159 KB
    libgfortran-3.0.1          |       h93005f0_2         495 KB
    libiconv-1.15              |       hdd342a3_7         1.3 MB
    libpng-1.6.37              |       ha441bb4_0         325 KB
    libsodium-1.0.16           |       h3efe00b_0         324 KB
    markupsafe-1.1.1           |   py37h1de35cc_0          28 KB
    matplotlib-3.0.3           |   py37h54f8f79_0         6.6 MB
    mistune-0.8.4              |   py37h1de35cc_0          54 KB
    mkl-2019.3                 |              199       154.7 MB
    mkl_fft-1.0.12             |   py37h5e564d8_0         155 KB
    mkl_random-1.0.2           |   py37h27c97d8_0         358 KB
    nbconvert-5.5.0            |             py_0         381 KB
    nbformat-4.4.0             |           py37_0         141 KB
    notebook-5.7.8             |           py37_0         7.3 MB
    numpy-1.16.3               |   py37hacdab7b_0          49 KB
    numpy-base-1.16.3          |   py37h6575580_0         4.2 MB
    pandas-0.24.2              |   py37h0a44026_0         9.9 MB
    pandoc-2.2.3.2             |                0        13.8 MB
    pandocfilters-1.4.2        |           py37_1          13 KB
    parso-0.4.0                |             py_0          66 KB
    pcre-8.43                  |       h0a44026_0         227 KB
    pexpect-4.7.0              |           py37_0          82 KB
    pickleshare-0.7.5          |           py37_0          12 KB
    pip-19.1.1                 |           py37_0         1.8 MB
    prometheus_client-0.6.0    |           py37_0          69 KB
    prompt_toolkit-2.0.9       |           py37_0         488 KB
    ptyprocess-0.6.0           |           py37_0          23 KB
    pygments-2.4.0             |             py_0         664 KB
    pyparsing-2.4.0            |             py_0          58 KB
    pyqt-5.9.2                 |   py37h655552a_2         4.4 MB
    pyrsistent-0.14.11         |   py37h1de35cc_0          88 KB
    python-3.7.3               |       h359304d_0        21.7 MB
    python-dateutil-2.8.0      |           py37_0         281 KB
    pytz-2019.1                |             py_0         236 KB
    pyzmq-18.0.0               |   py37h0a44026_0         457 KB
    qt-5.9.7                   |       h468cd18_1        76.8 MB
    qtconsole-4.4.4            |             py_0          88 KB
    send2trash-1.5.0           |           py37_0          16 KB
    setuptools-41.0.1          |           py37_0         635 KB
    sip-4.19.8                 |   py37h0a44026_0         252 KB
    sqlite-3.28.0              |       ha441bb4_0         2.3 MB
    terminado-0.8.2            |           py37_0          22 KB
    testpath-0.4.2             |           py37_0          91 KB
    tornado-6.0.2              |   py37h1de35cc_0         642 KB
    traitlets-4.3.2            |           py37_0         133 KB
    wcwidth-0.1.7              |           py37_0          23 KB
    webencodings-0.5.1         |           py37_1          19 KB
    wheel-0.33.4               |           py37_0          39 KB
    widgetsnbextension-3.4.2   |           py37_0         1.7 MB
    zeromq-4.3.1               |       h0a44026_3         565 KB
    ------------------------------------------------------------
                                           Total:       350.0 MB

The following NEW packages will be INSTALLED:

  appnope            pkgs/main/osx-64::appnope-0.1.0-py37_0
  attrs              pkgs/main/osx-64::attrs-19.1.0-py37_1
  backcall           pkgs/main/osx-64::backcall-0.1.0-py37_0
  blas               pkgs/main/osx-64::blas-1.0-mkl
  bleach             pkgs/main/osx-64::bleach-3.1.0-py37_0
  ca-certificates    pkgs/main/osx-64::ca-certificates-2019.1.23-0
  certifi            pkgs/main/osx-64::certifi-2019.3.9-py37_0
  cycler             pkgs/main/osx-64::cycler-0.10.0-py37_0
  dbus               pkgs/main/osx-64::dbus-1.13.6-h90a0687_0
  decorator          pkgs/main/osx-64::decorator-4.4.0-py37_1
  defusedxml         pkgs/main/noarch::defusedxml-0.6.0-py_0
  entrypoints        pkgs/main/osx-64::entrypoints-0.3-py37_0
  expat              pkgs/main/osx-64::expat-2.2.6-h0a44026_0
  freetype           pkgs/main/osx-64::freetype-2.9.1-hb4e5f40_0
  gettext            pkgs/main/osx-64::gettext-0.19.8.1-h15daf44_3
  glib               pkgs/main/osx-64::glib-2.56.2-hd9629dc_0
  icu                pkgs/main/osx-64::icu-58.2-h4b95b61_1
  intel-openmp       pkgs/main/osx-64::intel-openmp-2019.3-199
  ipykernel          pkgs/main/osx-64::ipykernel-5.1.0-py37h39e3cac_0
  ipython            pkgs/main/osx-64::ipython-7.5.0-py37h39e3cac_0
  ipython_genutils   pkgs/main/osx-64::ipython_genutils-0.2.0-py37_0
  ipywidgets         pkgs/main/osx-64::ipywidgets-7.4.2-py37_0
  jedi               pkgs/main/osx-64::jedi-0.13.3-py37_0
  jinja2             pkgs/main/osx-64::jinja2-2.10.1-py37_0
  jpeg               pkgs/main/osx-64::jpeg-9b-he5867d9_2
  jsonschema         pkgs/main/osx-64::jsonschema-3.0.1-py37_0
  jupyter            pkgs/main/osx-64::jupyter-1.0.0-py37_7
  jupyter_client     pkgs/main/osx-64::jupyter_client-5.2.4-py37_0
  jupyter_console    pkgs/main/osx-64::jupyter_console-6.0.0-py37_0
  jupyter_core       pkgs/main/osx-64::jupyter_core-4.4.0-py37_0
  kiwisolver         pkgs/main/osx-64::kiwisolver-1.1.0-py37h0a44026_0
  libcxx             pkgs/main/osx-64::libcxx-4.0.1-hcfea43d_1
  libcxxabi          pkgs/main/osx-64::libcxxabi-4.0.1-hcfea43d_1
  libedit            pkgs/main/osx-64::libedit-3.1.20181209-hb402a30_0
  libffi             pkgs/main/osx-64::libffi-3.2.1-h475c297_4
  libgfortran        pkgs/main/osx-64::libgfortran-3.0.1-h93005f0_2
  libiconv           pkgs/main/osx-64::libiconv-1.15-hdd342a3_7
  libpng             pkgs/main/osx-64::libpng-1.6.37-ha441bb4_0
  libsodium          pkgs/main/osx-64::libsodium-1.0.16-h3efe00b_0
  markupsafe         pkgs/main/osx-64::markupsafe-1.1.1-py37h1de35cc_0
  matplotlib         pkgs/main/osx-64::matplotlib-3.0.3-py37h54f8f79_0
  mistune            pkgs/main/osx-64::mistune-0.8.4-py37h1de35cc_0
  mkl                pkgs/main/osx-64::mkl-2019.3-199
  mkl_fft            pkgs/main/osx-64::mkl_fft-1.0.12-py37h5e564d8_0
  mkl_random         pkgs/main/osx-64::mkl_random-1.0.2-py37h27c97d8_0
  nbconvert          pkgs/main/noarch::nbconvert-5.5.0-py_0
  nbformat           pkgs/main/osx-64::nbformat-4.4.0-py37_0
  ncurses            pkgs/main/osx-64::ncurses-6.1-h0a44026_1
  notebook           pkgs/main/osx-64::notebook-5.7.8-py37_0
  numpy              pkgs/main/osx-64::numpy-1.16.3-py37hacdab7b_0
  numpy-base         pkgs/main/osx-64::numpy-base-1.16.3-py37h6575580_0
  openssl            pkgs/main/osx-64::openssl-1.1.1b-h1de35cc_1
  pandas             pkgs/main/osx-64::pandas-0.24.2-py37h0a44026_0
  pandoc             pkgs/main/osx-64::pandoc-2.2.3.2-0
  pandocfilters      pkgs/main/osx-64::pandocfilters-1.4.2-py37_1
  parso              pkgs/main/noarch::parso-0.4.0-py_0
  pcre               pkgs/main/osx-64::pcre-8.43-h0a44026_0
  pexpect            pkgs/main/osx-64::pexpect-4.7.0-py37_0
  pickleshare        pkgs/main/osx-64::pickleshare-0.7.5-py37_0
  pip                pkgs/main/osx-64::pip-19.1.1-py37_0
  prometheus_client  pkgs/main/osx-64::prometheus_client-0.6.0-py37_0
  prompt_toolkit     pkgs/main/osx-64::prompt_toolkit-2.0.9-py37_0
  ptyprocess         pkgs/main/osx-64::ptyprocess-0.6.0-py37_0
  pygments           pkgs/main/noarch::pygments-2.4.0-py_0
  pyparsing          pkgs/main/noarch::pyparsing-2.4.0-py_0
  pyqt               pkgs/main/osx-64::pyqt-5.9.2-py37h655552a_2
  pyrsistent         pkgs/main/osx-64::pyrsistent-0.14.11-py37h1de35cc_0
  python             pkgs/main/osx-64::python-3.7.3-h359304d_0
  python-dateutil    pkgs/main/osx-64::python-dateutil-2.8.0-py37_0
  pytz               pkgs/main/noarch::pytz-2019.1-py_0
  pyzmq              pkgs/main/osx-64::pyzmq-18.0.0-py37h0a44026_0
  qt                 pkgs/main/osx-64::qt-5.9.7-h468cd18_1
  qtconsole          pkgs/main/noarch::qtconsole-4.4.4-py_0
  readline           pkgs/main/osx-64::readline-7.0-h1de35cc_5
  send2trash         pkgs/main/osx-64::send2trash-1.5.0-py37_0
  setuptools         pkgs/main/osx-64::setuptools-41.0.1-py37_0
  sip                pkgs/main/osx-64::sip-4.19.8-py37h0a44026_0
  six                pkgs/main/osx-64::six-1.12.0-py37_0
  sqlite             pkgs/main/osx-64::sqlite-3.28.0-ha441bb4_0
  terminado          pkgs/main/osx-64::terminado-0.8.2-py37_0
  testpath           pkgs/main/osx-64::testpath-0.4.2-py37_0
  tk                 pkgs/main/osx-64::tk-8.6.8-ha441bb4_0
  tornado            pkgs/main/osx-64::tornado-6.0.2-py37h1de35cc_0
  traitlets          pkgs/main/osx-64::traitlets-4.3.2-py37_0
  wcwidth            pkgs/main/osx-64::wcwidth-0.1.7-py37_0
  webencodings       pkgs/main/osx-64::webencodings-0.5.1-py37_1
  wheel              pkgs/main/osx-64::wheel-0.33.4-py37_0
  widgetsnbextension pkgs/main/osx-64::widgetsnbextension-3.4.2-py37_0
  xz                 pkgs/main/osx-64::xz-5.2.4-h1de35cc_4
  zeromq             pkgs/main/osx-64::zeromq-4.3.1-h0a44026_3
  zlib               pkgs/main/osx-64::zlib-1.2.11-h1de35cc_3


Proceed ([y]/n)? y


Downloading and Extracting Packages
pyzmq-18.0.0         | 457 KB    | ####################################################################################################################################### | 100%
pip-19.1.1           | 1.8 MB    | ####################################################################################################################################### | 100%
terminado-0.8.2      | 22 KB     | ####################################################################################################################################### | 100%
sqlite-3.28.0        | 2.3 MB    | ####################################################################################################################################### | 100%
wcwidth-0.1.7        | 23 KB     | ####################################################################################################################################### | 100%
expat-2.2.6          | 129 KB    | ####################################################################################################################################### | 100%
parso-0.4.0          | 66 KB     | ####################################################################################################################################### | 100%
prompt_toolkit-2.0.9 | 488 KB    | ####################################################################################################################################### | 100%
setuptools-41.0.1    | 635 KB    | ####################################################################################################################################### | 100%
numpy-base-1.16.3    | 4.2 MB    | ####################################################################################################################################### | 100%
jupyter_client-5.2.4 | 127 KB    | ####################################################################################################################################### | 100%
dbus-1.13.6          | 560 KB    | ####################################################################################################################################### | 100%
jpeg-9b              | 236 KB    | ####################################################################################################################################### | 100%
backcall-0.1.0       | 20 KB     | ####################################################################################################################################### | 100%
cycler-0.10.0        | 14 KB     | ####################################################################################################################################### | 100%
ipython-7.5.0        | 1.1 MB    | ####################################################################################################################################### | 100%
libsodium-1.0.16     | 324 KB    | ####################################################################################################################################### | 100%
mistune-0.8.4        | 54 KB     | ####################################################################################################################################### | 100%
ipywidgets-7.4.2     | 151 KB    | ####################################################################################################################################### | 100%
defusedxml-0.6.0     | 23 KB     | ####################################################################################################################################### | 100%
sip-4.19.8           | 252 KB    | ####################################################################################################################################### | 100%
attrs-19.1.0         | 56 KB     | ####################################################################################################################################### | 100%
pandas-0.24.2        | 9.9 MB    | ####################################################################################################################################### | 100%
mkl-2019.3           | 154.7 MB  | ####################################################################################################################################### | 100%
pcre-8.43            | 227 KB    | ####################################################################################################################################### | 100%
gettext-0.19.8.1     | 3.4 MB    | ####################################################################################################################################### | 100%
webencodings-0.5.1   | 19 KB     | ####################################################################################################################################### | 100%
python-dateutil-2.8. | 281 KB    | ####################################################################################################################################### | 100%
ipython_genutils-0.2 | 39 KB     | ####################################################################################################################################### | 100%
freetype-2.9.1       | 864 KB    | ####################################################################################################################################### | 100%
numpy-1.16.3         | 49 KB     | ####################################################################################################################################### | 100%
libedit-3.1.20181209 | 159 KB    | ####################################################################################################################################### | 100%
mkl_random-1.0.2     | 358 KB    | ####################################################################################################################################### | 100%
widgetsnbextension-3 | 1.7 MB    | ####################################################################################################################################### | 100%
zeromq-4.3.1         | 565 KB    | ####################################################################################################################################### | 100%
libgfortran-3.0.1    | 495 KB    | ####################################################################################################################################### | 100%
pickleshare-0.7.5    | 12 KB     | ####################################################################################################################################### | 100%
testpath-0.4.2       | 91 KB     | ####################################################################################################################################### | 100%
pandocfilters-1.4.2  | 13 KB     | ####################################################################################################################################### | 100%
kiwisolver-1.1.0     | 60 KB     | ####################################################################################################################################### | 100%
pyrsistent-0.14.11   | 88 KB     | ####################################################################################################################################### | 100%
jupyter-1.0.0        | 6 KB      | ####################################################################################################################################### | 100%
blas-1.0             | 5 KB      | ####################################################################################################################################### | 100%
intel-openmp-2019.3  | 1.1 MB    | ####################################################################################################################################### | 100%
python-3.7.3         | 21.7 MB   | ####################################################################################################################################### | 100%
tornado-6.0.2        | 642 KB    | ####################################################################################################################################### | 100%
jinja2-2.10.1        | 188 KB    | ####################################################################################################################################### | 100%
wheel-0.33.4         | 39 KB     | ####################################################################################################################################### | 100%
pyqt-5.9.2           | 4.4 MB    | ####################################################################################################################################### | 100%
appnope-0.1.0        | 8 KB      | ####################################################################################################################################### | 100%
entrypoints-0.3      | 12 KB     | ####################################################################################################################################### | 100%
prometheus_client-0. | 69 KB     | ####################################################################################################################################### | 100%
pygments-2.4.0       | 664 KB    | ####################################################################################################################################### | 100%
nbformat-4.4.0       | 141 KB    | ####################################################################################################################################### | 100%
ptyprocess-0.6.0     | 23 KB     | ####################################################################################################################################### | 100%
jupyter_core-4.4.0   | 63 KB     | ####################################################################################################################################### | 100%
mkl_fft-1.0.12       | 155 KB    | ####################################################################################################################################### | 100%
bleach-3.1.0         | 221 KB    | ####################################################################################################################################### | 100%
glib-2.56.2          | 4.7 MB    | ####################################################################################################################################### | 100%
matplotlib-3.0.3     | 6.6 MB    | ####################################################################################################################################### | 100%
jedi-0.13.3          | 236 KB    | ####################################################################################################################################### | 100%
pyparsing-2.4.0      | 58 KB     | ####################################################################################################################################### | 100%
notebook-5.7.8       | 7.3 MB    | ####################################################################################################################################### | 100%
markupsafe-1.1.1     | 28 KB     | ####################################################################################################################################### | 100%
nbconvert-5.5.0      | 381 KB    | ####################################################################################################################################### | 100%
traitlets-4.3.2      | 133 KB    | ####################################################################################################################################### | 100%
pandoc-2.2.3.2       | 13.8 MB   | ####################################################################################################################################### | 100%
send2trash-1.5.0     | 16 KB     | ####################################################################################################################################### | 100%
icu-58.2             | 22.3 MB   | ####################################################################################################################################### | 100%
qtconsole-4.4.4      | 88 KB     | ####################################################################################################################################### | 100%
jupyter_console-6.0. | 35 KB     | ####################################################################################################################################### | 100%
decorator-4.4.0      | 18 KB     | ####################################################################################################################################### | 100%
pytz-2019.1          | 236 KB    | ####################################################################################################################################### | 100%
ipykernel-5.1.0      | 156 KB    | ####################################################################################################################################### | 100%
jsonschema-3.0.1     | 88 KB     | ####################################################################################################################################### | 100%
qt-5.9.7             | 76.8 MB   | ####################################################################################################################################### | 100%
pexpect-4.7.0        | 82 KB     | ####################################################################################################################################### | 100%
libpng-1.6.37        | 325 KB    | ####################################################################################################################################### | 100%
libiconv-1.15        | 1.3 MB    | ####################################################################################################################################### | 100%
Preparing transaction: done
Verifying transaction: done
Executing transaction: done
```

```
(notebook) 05/30 00:38:08 $ conda install xlrd
Collecting package metadata: done
Solving environment: done

## Package Plan ##

  environment location: /usr/local/miniconda3/envs/notebook

  added / updated specs:
    - xlrd


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    xlrd-1.2.0                 |           py37_0         186 KB
    ------------------------------------------------------------
                                           Total:         186 KB

The following NEW packages will be INSTALLED:

  xlrd               pkgs/main/osx-64::xlrd-1.2.0-py37_0


Proceed ([y]/n)? y


Downloading and Extracting Packages
xlrd-1.2.0           | 186 KB    | ############################################# | 100%
Preparing transaction: done
Verifying transaction: done
Executing transaction: done
```


### 2019/06/18

pyenv で入れ直すために、miniconda をアンインストール。たぶん公式のインストーラで入れた奴だと思う。
brew list には含まれていなかった。

https://docs.conda.io/projects/conda/en/latest/user-guide/install/macos.html?highlight=miniconda#

```
rm -rf /usr/local/miniconda3
rm -rf ~/.conda
```

以下を実行

```
$ pyenv install miniconda3.4.3.30
$ pyenv local miniconda3-4.3.30
$ conda create -n jupyternote python=3.6.3
$ pyenv uninstall miniconda3-4.3.30/envs/jupyternote
```

https://qiita.com/KRiver1/items/f3c0478c5a430ce06aa8
https://github.com/pyenv/pyenv-virtualenv/issues/178


### 2019/07/02

pyenv local miniconda3-4.3.30 を実行した。


### 2019/07/03

```
$ conda install numpy pandas matplotlib jupyter notebook xlrd
```
を実行した。