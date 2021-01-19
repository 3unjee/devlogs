# Configure and build VLC from scratch

## Ubuntu
- *Install Ubuntu 20.04 LTS*

## Qt
- *Install Qt 5.11.3* -> Desktop Gcc 64-bit module:
    - https://download.qt.io/new_archive/qt/5.11/5.11.3

## Configure
- `sudo apt install git build-essential pkg-config libtool automake autopoint gettext`
- `sudo apt install python`         # NOTE: This is required for building 'tools'
- `sudo apt install cmake`          # NOTE: This is required for building 'contrib'
- `sudo apt install libxcb-xkb-dev` # NOTE: This is required for building 'vlc'
- *Enable sources on Ubuntu* (https://askubuntu.com/questions/496549/error-you-must-put-some-source-uris-in-your-sources-list)
- `sudo apt-get build-dep vlc`

## Configure
- *Optional*:
    - fork https://code.videolan.org/videolan/vlc
- Generate rsa: `ssh-keygen -t rsa -b 2048 -C "bunjee@omega.gg"`
- Upload {YOUR_HOME}/.ssh/id_rsa.pub to code.videolan.org
- `sudo apt install git`
- git clone https://code.videolan.org/{$YOUR_FORK}/vlc

## VLC tools
- `cd extra/tools`
- `./bootstrap`
- `make -j4`

## VLC contrib
- `cd ../../contrib`
- `mkdir contrib-nativ`
- `cd contrib-nativ`
- `../bootstrap`
- `make -j4`

## VLC
- `cd ../..`
- `./bootstrap`
- `mkdir build-qt11`
- `cd build-qt11`
- `../configure '--disable-optimizations' '--enable-debug' '--disable-nls' '--without-kde-solid' '--enable-qt-qml-cache' '--enable-qt-qml-debug' '--disable-skins2' '--disable-upnp' '--disable-chromecast' '--disable-srt' '--disable-aom' '--disable-bluray' 'CFLAGS=-ggdb -O0 -fno-omit-frame-pointer' 'PKG_CONFIG_PATH={YOUR_HOME}/Qt/Qt5.11.3/5.11.3/gcc_64/lib/pkgconfig/:{YOUR_HOME}/dev/videolan/vlc/contrib/x86_64-linux-gnu/lib/pkgconfig'`
- `make -j4`
