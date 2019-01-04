# tvheadend-xboxone-tuner
This guide will give you the possibility to use your Xbox One TV tuner with TVHeadend on Debian

- su

- apt install git make patchutils libproc-processtable-perl firmware-misc-nonfree
- apt install linux-headers-`uname -r` linux-source

From Home directory

- mkdir xboxone
- cd xboxone
- wget http://palosaari.fi/linux/v4l-dvb/firmware/MN88472/02/latest/dvb-demod-mn88472-02.fw
- cp dvb-demod-mn88472-02.fw /lib/firmware
- mkdir linuxtv
- git clone git://linuxtv.org/media_build.git
- git clone --depth=1 https://github.com/trsqr/media_tree.git -b xboxone ./media
- cd media_build
- git reset --hard 9ccb87d
- make dir DIR=../media
- make distclean
- make

- make install

- reboot
