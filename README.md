# rpi-dotfiles

Dotfiles for Raspberry Pi

# Table of Contents

* [Setup](#setup)
  * [Raspbian Wheezy](#raspbian-wheezy)
  * [Arch Linux Arm](#arch-linux-arm)
* [See Also](#see-also)

# Setup

## Raspbian Wheezy

```bash
# rpi-d
sudo bash
nano /etc/network/interfaces
# os x internet sharing
iface eth0 inet dhcp
/etc/init.d/networking restart
# 192.168.2.x
sudo bash
apt-get update
apt-get upgrade -y
# redis
apt-get install -y redis-server python-redis libhiredis-dev libhiredis-dbg libhiredis0.10
# sqlite
apt-get install -y sqlite3 libsqlite-tcl python-pysqlite2
# ssh ssl crypto
apt-get install -y libcrypto++-dev libcrypto++9 libcrypto++9-dbg libcrypto++-utils
# speech synthesis
apt-get install -y espeak espeak-data espeak-dbg espeakup python-espeak
# email
apt-get install -y ssmtp mailutils
# configure audio for headphone jack
amixer cset numid=1
exit
mkdir ~/Codebase
cd ~/Codebase
git config --global user.email "reid.parham@gmail.com"
git config --global user.name "parhamr"
cat ~/.ssh/id_dsa.pub
# add to GitHub account
git clone git@github.com:parhamr/rpi-dotfiles.git
```

## Arch Linux ARM

# See Also


