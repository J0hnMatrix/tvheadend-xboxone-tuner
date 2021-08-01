# tvheadend-xboxone-tuner
This guide will give you the possibility to use your Xbox One TV tuner with TVHeadend on Debian
As of updating this guide, one the a firmware file is now needed to copied into /lib/firmware

From Home directory

```console
mkdir xboxone
cd xboxone
wget http://palosaari.fi/linux/v4l-dvb/firmware/MN88472/02/latest/dvb-demod-mn88472-02.fw
sudo cp dvb-demod-mn88472-02.fw /lib/firmware

reboot
```
