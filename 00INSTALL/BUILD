BUILD
Created Sat Nov 16 09:34:19 AKST 2013
Copyright (C) 2013 by Raymond E. Marcil <marcilr@gmail.com>


Build HandBrake open source video transcoder

1. Expand tarball
$ tar jxvpf HandBrake-0.9.9.tar.bz2

2. Resolve build dependencies:

Debian wheezy packages:
  automake - Tool for generating GNU Standards-compliant Makefiles (Nov 16, 2013)
  build-essential - Informational list of build-essential packages (Nov 16, 2013)
  gcc - GNU C compiler (Nov 16, 2013)
  libtool - Generic library support script (Nov 16, 2013)
  make - An utility for Directing compilation. (Sep  3, 2013)
  yasm - modular assembler with multiple syntaxes support
    NOTE: This install yasm 1.1.0 but HandBrake 0.9.9 required 1.2.0.
    Downloaded, compiled, and installed from source.

    $ tar zxvpf 00TARBALLS/dev/yasm-1.2.0.tar.gz
    $ ./configure --prefix=/usr/local
    $ make
    # make install
    # ldconfig

intltool - Utility scripts for internationalizing XML (Nov 16, 2013)
libappindicator-dev - allow applications to export a menu into the panel -- development (Nov 16, 2013)
libass-dev - development files for libass (Nov 16, 2013)
libbz2-dev - high-quality block-sorting file compressor library - development (Nov 16, 2013)
libdbus-glib-1-dev - simple interprocess messaging system (GLib interface) (Nov 16, 2013)
libfontconfig1-dev - generic font configuration library - development (Nov 16, 2013)
libfreetype6-dev - FreeType 2 font engine, development files (Nov 16, 2013)
libfribidi-dev - Development files for FreeBidi library (Nov 16, 2013)
libglib2.0-dev - Development files for the GLib library (Nov 16, 2013)
libgstreamer0.10-dev - GStreamer core development files (Nov 16, 2013)
libgstreamer-plugins-base0.10-dev - GStreamer development files for libraries from the "base" set
  (Nov 16, 2013)
libgtk2.0-dev - development files for the GTK+ library (Nov 16, 2013)
libgudev-1.0-dev - libgudev-1.0 development files (Nov 16, 2013)
libnotify-dev - sends desktop notifications to a notification daemon (Development files) (Nov 16, 2013)
libogg-dev - Ogg bitstream library development files (Nov 16, 2013)
libsamplerate0-dev - Development files for audio sample rate conversion (Nov 16, 2013)
libtheora-dev - The Theora Video Compression Codec (development files) (Nov 16, 2013)
libvorbis-dev - The Vorbis General Audio Compression Codec (development files) (Nov 16, 2013)
libwebkit-dev - Transitional package for the development files of WebKitGTK+ (Nov 16, 2013)
libxml2-dev - Development files for the GNOME XML library (Nov 16, 2013)
zlib1g-dev - compression library - development (Nov 16, 2013)

To install these packages:

# aptitude install subversion yasm build-essential autoconf libtool \
zlib1g-dev libbz2-dev libogg-dev libtheora-dev libvorbis-dev \
libsamplerate-dev libxml2-dev libfribidi-dev libfreetype6-dev \
libfontconfig1-dev libass-dev intltool libglib2.0-dev libdbus-glib-1-dev \
libgtk2.0-dev libgudev-1.0-dev libwebkit-dev libnotify-dev \
libgstreamer0.10-dev libgstreamer-plugins-base0.10-dev libappindicator-dev


3. Configure
$ ./configure --prefix=/usr/local/handbrake --force
probe: host tuple...(pass) x86_64-unknown-linux-gnu
compute: available architectures...(pass) x86_64
find: ar...(pass) /usr/bin/ar
find: cp...(pass) /bin/cp
find: curl...(pass) /usr/bin/curl
find: gcc...(pass) /usr/bin/gcc
find: gmake...(pass) /usr/bin/make
find: m4...(pass) /usr/bin/m4
find: mkdir...(pass) /bin/mkdir
find: gpatch...(pass) /usr/bin/patch
find: rm...(pass) /bin/rm
find: ranlib...(pass) /usr/bin/ranlib
find: strip...(pass) /usr/bin/strip
find: gtar...(pass) /bin/tar
find: wget...(pass) /usr/bin/wget
find: yasm...(pass) /usr/local/bin/yasm
find: autoconf...(pass) /usr/bin/autoconf
find: automake...(pass) /usr/bin/automake
find: libtool...(pass) /usr/bin/libtool
find: xcodebuild...(fail) not found
find: lipo...(fail) not found
select: fetch...(pass) wget (/usr/bin/wget)
compute: build tuple...(pass) x86_64-unknown-linux-gnu
probe: number of CPU cores...(pass) 4
probe: svn info...(fail) code 1
compute: project data...(pass) HandBrake (unofficial)
version probe: yasm...(pass) 1.2.0
compute: makevar SRC/    = ..
compute: makevar BUILD/  = .
compute: makevar PREFIX/ = /usr/local/handbrake
chdir: ./build
write: GNUmakefile
write: project/handbrake.m4
-------------------------------------------------------------------------------
Build is configured!
You may now cd into ./build and run make (/usr/bin/make).
$

NOTE: Used --force option to overwrite prior build directory.


4. Compile source
$ cd build
build$ time make
...
libtool: link: g++ -g -O2 -D_ENABLE_GST -D_USE_APP_IND -Wl,--export-dynamic -Wl,--exclude-libs \
-Wl,ALL -Wl,-S -g0 -O3 -o ghb callbacks.o queuehandler.o audiohandler.o subtitlehandler.o \
x264handler.o main.o settings.o resources.o presets.o preview.o icons.o icon_tools.o values.o \
appcast.o plist.o hb-backend.o renderer_button.o ghbcellrenderertext.o ghbcompositor.o ghb-dvd.o \
marshalers.o -pthread  -L/usr/local/src/HandBrake-0.9.9/build//libhb \
-L/usr/local/src/HandBrake-0.9.9/build//contrib/lib -lhb \
/usr/local/src/HandBrake-0.9.9/build/contrib/lib/liba52.a \
-L/usr/local/src/HandBrake-0.9.9/build/contrib/lib \
/usr/local/src/HandBrake-0.9.9/build/contrib/lib/libmkv.a -lavresample -lavformat -lavcodec \
-lavutil /usr/local/src/HandBrake-0.9.9/build/contrib/lib/libdvdnav.a \
/usr/local/src/HandBrake-0.9.9/build/contrib/lib/libdvdread.a \
/usr/local/src/HandBrake-0.9.9/build/contrib//lib/libfaac.a \
/usr/local/src/HandBrake-0.9.9/build/contrib//lib/libmp3lame.a -lm \
/usr/local/src/HandBrake-0.9.9/build/contrib//lib/libmpeg2.a \
/usr/lib/x86_64-linux-gnu/libvorbis.so /usr/lib/x86_64-linux-gnu/libvorbisenc.so -logg \
-lsamplerate -lx264 /usr/local/src/HandBrake-0.9.9/build/contrib/lib/libmp4v2.a -lswscale \
-ltheoraenc -ltheoradec -lz -lbz2 /usr/local/src/HandBrake-0.9.9/build/contrib/lib/libbluray.a \
-ldl -lpthread -lass -lnotify -ldbus-glib-1 -ldbus-1 -lgudev-1.0 -lgstvideo-0.10 -lgstaudio-0.10 \
/usr/lib/x86_64-linux-gnu/libgstbase-0.10.so -lgstinterfaces-0.10 -lgstpbutils-0.10 \
/usr/lib/x86_64-linux-gnu/libgstreamer-0.10.so -lgmodule-2.0 -lgthread-2.0 -lrt -lxml2 \
-lwebkitgtk-1.0 -lsoup-2.4 -ljavascriptcoregtk-1.0 -lappindicator -ldbusmenu-glib -lgtk-x11-2.0 \
-lgdk-x11-2.0 -latk-1.0 -lgio-2.0 -lpangoft2-1.0 -lpangocairo-1.0 -lgdk_pixbuf-2.0 \
/usr/lib/x86_64-linux-gnu/libcairo.so -lpango-1.0 /usr/lib/x86_64-linux-gnu/libfreetype.so \
-lfontconfig -lgobject-2.0 -lglib-2.0 -pthread
make[3]: Leaving directory `/usr/local/src/HandBrake-0.9.9/build/gtk/src'
Making all in po
make[3]: Entering directory `/usr/local/src/HandBrake-0.9.9/build/gtk/po'
make[3]: Nothing to be done for `all'.
make[3]: Leaving directory `/usr/local/src/HandBrake-0.9.9/build/gtk/po'
make[3]: Entering directory `/usr/local/src/HandBrake-0.9.9/build/gtk'
make[3]: Nothing to be done for `all-am'.
make[3]: Leaving directory `/usr/local/src/HandBrake-0.9.9/build/gtk'
make[2]: Leaving directory `/usr/local/src/HandBrake-0.9.9/build/gtk'
make[1]: Leaving directory `/usr/local/src/HandBrake-0.9.9/build/gtk'

real    17m36.497s
user    14m13.701s
sys     1m6.996s
build$

Looks good!

5. Install it
build# make install
/bin/mkdir -p /usr/local/handbrake/bin
/bin/cp ./HandBrakeCLI /usr/local/handbrake/bin/HandBrakeCLI
make -C ./gtk/ prefix=/usr/local/handbrake install
make[1]: Entering directory `/usr/local/src/HandBrake-0.9.9/build/gtk'
Making install in src
make[2]: Entering directory `/usr/local/src/HandBrake-0.9.9/build/gtk/src'
make[3]: Entering directory `/usr/local/src/HandBrake-0.9.9/build/gtk/src'
 /bin/mkdir -p '/usr/local/handbrake/bin'
...
make[2]: Leaving directory `/usr/local/src/HandBrake-0.9.9/build/gtk/po'
make[2]: Entering directory `/usr/local/src/HandBrake-0.9.9/build/gtk'
make[3]: Entering directory `/usr/local/src/HandBrake-0.9.9/build/gtk'
make[3]: Nothing to be done for `install-exec-am'.
make[3]: Nothing to be done for `install-data-am'.
make[3]: Leaving directory `/usr/local/src/HandBrake-0.9.9/build/gtk'
make[2]: Leaving directory `/usr/local/src/HandBrake-0.9.9/build/gtk'
make[1]: Leaving directory `/usr/local/src/HandBrake-0.9.9/build/gtk'
build#

Set privs on /usr/local/handbrake/ directory:
build# chown -R marcilr:marcilr /usr/local/handbrake/


6. Inspection
$ cd /usr/local/handbrake
handbrake$ ls
bin  share
$

handbrake$ ls bin
ghb  HandBrakeCLI
handbrake$


7. Test it
$ cd /usr/local/handbrake/bin
handbrake$ ./ghb &

HandBrake 0.9.9 looks great!

8. Create handbrake symlimk to /usr/local/bin:
# ln -s /usr/local/handbrake/bin/ghb /usr/local/bin/handbrake


Filelist
========
HandBrake-0.9.9/configure
  Configuration script.

HandBrake-0.9.9/doc/BUILD-Linux
  Guide to Building HandBrake svn5208 (2013012701) on Linux



Links
=====
HandbBrake
The open source video transcoder
http://handbrake.fr/

