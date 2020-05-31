## rtl8188eus v5.3.9

# Realtek rtl8188eus &amp; rtl8188eu &amp; rtl8188etv WiFi drivers

This method works for all Realtek wifi dongles which not support monitor mode

# Installation process

extract the zip
open new terminal in folder
type the following commands (only for first time)
~~~~~~~~~~~~~~~~~~~~~~~~~
sudo make
sudo make install
~~~~~~~~~~~~~~~~~~~~~~~~~

# MONITOR MODE howto use for linux,parrot os
Use these steps to enter monitor mode.

# For linux

``` 
rmmod r8188eu.ko
sudo -i
echo "blacklist r8188eu.ko">"/etc/modprobe.d/realtek.conf"
exit
make install
modprobe 8188eu
iwconfig
iw dev wlan0 set type monitor
```
# For parrot os

~~~~
rmmod r8188eu.ko

sudo -i

sudo echo "blacklist r8188eu.ko">"/etc/modprobe.d/realtek.conf"

cd /home/user/Downloads/rtl8188eus    (change you directory loaction)

make install

modprobe 8188eu

iwconfig

sudo iw dev wlan0 set type monitor  (see the wifi module name and change wlan0 to your module name because parrot os has different name)
~~~~~~~~~

# check for monitor mode

iwconfig
see that wlan0 is auto then type " iw dev wlan0 set type monitor "
to get monitor mode



# Credits
Realtek       - https://www.realtek.com<br>
Alfa Networks - https://www.alfa.com.tw<br>
aircrack-ng.  - https://www.aircrack-ng.org<br>
<br>
And all those who may be using or contributing to it of anykind. Thanks!<br>
