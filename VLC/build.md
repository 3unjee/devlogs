# Configure and build VLC from scratch

## Ubuntu
- Install Ubuntu 22.04 LTS

## Qt
- `sudo apt-get install libxcb-xinerama0`  # NOTE: This is required for running Qt installation file
- Install Qt 5.11.3 and Qt 5.15.2 -> Desktop Gcc 64-bit module:
    - https://download.qt.io/official_releases/online_installers/
    - Upon installation, select to show 'Archives' in order to install both 5.11.3 and 5.15.2

## Install
- `sudo apt install git build-essential pkg-config libtool automake autopoint gettext`
- `sudo apt install cmake`          # NOTE: This is required for building 'contrib'
- `sudo apt install libxcb-xkb-dev qtdeclarative5-dev qtquickcontrols2-5-dev` # NOTE: This is required for building 'vlc'
- `sudo apt-get install qml-module-qtgraphicaleffects qml-module-qtqml-models2 qml-module-qtquick-controls2 qml-module-qtquick-layouts qml-module-qtquick-templates2` # NOTE: This is required for running 'vlc'
- Enable sources on Ubuntu (https://askubuntu.com/questions/496549/error-you-must-put-some-source-uris-in-your-sources-list)
- `sudo apt-get build-dep vlc`

## Clone
- Optional:
    - fork https://code.videolan.org/videolan/vlc
- Generate rsa: `ssh-keygen -t rsa -b 2048 -C "{YOUR_EMAIL}"`
- Upload {YOUR_HOME}/.ssh/id_rsa.pub to code.videolan.org
- git clone https://code.videolan.org/{$YOUR_FORK}/vlc

## VLC tools
- `cd vlc/extras/tools`
- `./bootstrap`
- `make -j4`

## VLC contrib
- `cd ../../contrib`
- `mkdir contrib-nativ`
- `cd contrib-nativ`
- `../bootstrap --disable-gcrypt --disable-bluray`
- `make -j4`

## VLC
- `cd ../..`
- `./bootstrap`
- `mkdir build-qt11`
- `cd build-qt11`
- `../configure '--disable-optimizations' '--enable-debug' '--disable-nls' '--without-kde-solid' '--enable-qt-qml-cache' '--enable-qt-qml-debug' '--disable-skins2' '--disable-upnp' '--disable-chromecast' '--disable-srt' '--disable-aom' '--disable-bluray' 'CFLAGS=-ggdb -O0 -fno-omit-frame-pointer' 'PKG_CONFIG_PATH=$HOME/Qt/5.11.3/gcc_64/lib/pkgconfig/:$HOME/vlc/contrib/x86_64-linux-gnu/lib/pkgconfig'`
- `make -j4`
