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
nano .ssh/authorized_keys
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
nano /etc/ssmtp/ssmtp.conf
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

```bash
nano .ssh/authorized_keys
systemctl disable network@eth0.service
systemctl stop network@eth0.service
# power cycle; DHCP should auto configure on next boot
pacman -Syu
# Redis
pacman -S redis
# SQLite
pacman -S sqlite sqlite-tcl
# speech synthesizer: espeak
pacman -S espeak
# email
pacman -S ssmtp
# config: smtp.sendgrid.net:587
nano /etc/ssmtp/ssmtp.conf
# Git
pacman -S git
```


# See Also


