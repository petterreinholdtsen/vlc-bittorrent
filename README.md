# vlc-bittorrent (Bittorrent plugin for VLC)

## What is this?

With vlc-bittorrent, you can open a **.torrent** file or **magnet link** with VLC and stream any media that it contains.

## Dependencies (on Linux)

* libvlc core ("libvlccore8" in Debian/Ubuntu)
* libtorrent ("libtorrent-rasterbar9" in Debian/Ubuntu)

## Building from git on a recent Debian/Ubuntu

    $ sudo apt-get install autoconf automake libtool make libvlccore-dev libtorrent-rasterbar-dev g++
    $ git clone https://github.com/johang/vlc-bittorrent.git vlc-bittorrent
    $ cd vlc-bittorrent
    $ autoreconf -i
    $ ./configure --prefix=/tmp/vlc
    $ make

And optionally, if you want to install it:

    $ make install

Then, to load it in VLC player:

    $ VLC_PLUGIN_PATH=/tmp/vlc vlc --no-plugins-cache video.torrent
