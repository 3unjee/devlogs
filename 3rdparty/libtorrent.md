# libtorrent

## Building libtorrent on Windows

### Requirements

- MinGW 7.3.0: https://sourceforge.net/projects/mingw.
- Boost 1.53.0: http://www.boost.org/users/history/version_1_53_0.html.
- Boost 1.55.0: http://www.boost.org/users/history/version_1_55_0.html.
- libtorrent 1.1.12: https://github.com/arvidn/libtorrent/releases

Note: Extract everything in the same folder.


### Configure

Copy and run this batch file:

    set folder=C:\libtorrent

    set PATH=%PATH%;%folder%\MinGW\bin;%folder%\boost_1_53_0\tools\build\v2\engine\bin.ntx86;%folder%\boost_1_55_0

    set BOOST_BUILD_PATH=%folder%\boost_1_55_0\tools\build\v2

    set BOOST_ROOT=%folder%\boost_1_55_0

Note: Set "folder" with your own path.

- Go to "folder/boost_1_53_0/tools/build/v2".
- Edit "user-config.jam" and uncomment "using gcc".

- Go to "folder/boost_1_55_0/tools/build/v2".
- Edit "user-config.jam" and uncomment "using gcc".


### Build

- Go to "folder/boost_1_53_0/tools/build/v2/engine".
- Run "build.bat gcc".

- Go to "folder/libtorrent".
- Run "bjam gcc link=static runtime-link=static variant=release warnings=off".

Note: For some reason you have to rename "utp-stream.o" to "utp-stram.o" to make it link.


## Related

(MotionBox #1) Torrent streaming: [MotionBox/chapters/1.TorrentStreaming.md](../MotionBox/chapters/1.TorrentStreaming.md)


## Author

Benjamin Arnaud aka [bunjee](https://bunjee.me) | <bunjee@omega.gg>.
