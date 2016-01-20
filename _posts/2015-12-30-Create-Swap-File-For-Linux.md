---
layout: post
title:  Create swap file for Linux
---


### Create swap files


\> dd if=/dev/zero of=/tmp/swap_file bs=512k count=4000

\> mkswap /tmp/swap_file 

\> swapon /tmp/swap_file  

### Add the following item to fstab for auto mounting

/tmp/swap swap swap defaults 0 0

### Modify Swapness

* for once

sudo sysctl vm.swappiness=10 

* for permanently

sudo vim /etc/sysctl.conf

+ vm.swappiness=10 