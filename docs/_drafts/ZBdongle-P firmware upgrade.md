---
layout: post
title:  "Upgrade Firmware on ZBDongle-P"
date:   2023-01-27 13:38:43 +1000
last_modified_at: 2023-01-26 22:01:21 +1100
description: Upgrade firmware instructions
featured_image: /assets/img/sections/mark-harrison.jpg
categories: 
  - Home Assistant
---


#### Backup
Before you begin take a backup of your existing network. 
ZHA - This can be done through the UI 
Zigbee2MQTT - Make a backup of the files in `/config/zigbee2mqtt`
#### Dependencies
Windows install [python for windows](https://www.python.org/downloads/)
If you are using Linux Python will already be installed. 

You will need to make sure you have all dependencies installed, so run the following command from a terminal.
`pip install pyserial python-magic intelhex`

#### cc2538-bsl
Download and unzip the `cc2538-bsl` tool:
https://github.com/JelmerT/cc2538-bsl/archive/refs/tags/2.1.zip

Firmware
https://github.com/Koenkk/Z-Stack-firmware/blob/master/coordinator/Z-Stack_3.x.0/bin/CC1352P2_CC2652P_launchpad_coordinator_20220219.zip?raw=true

Flash with cc2538-bsl
```
$ ./cc2538-bsl.py -e -w -v -p /dev/ttyUSB0 --bootloader-sonoff-usb ./CC1352P2_CC2652P_launchpad_coordinator_20220219.hex
``` 