# tvheadend-xboxone-tuner
This guide will give you the possibility to use your Xbox One TV tuner with TVHeadend on Debian

- sudo apt install git make patchutils libproc-processtable-perl
- sudo apt install linux-headers-`uname -r` linux-source

From your home directory

- mkdir linuxtv
- git clone git://linuxtv.org/media_build.git
- git clone --depth=1 https://github.com/trsqr/media_tree.git -b xboxone ./media
- cd media_build
- git reset --hard 9ccb87d
- make dir DIR=../media
- make distclean
- make

- sudo make install
