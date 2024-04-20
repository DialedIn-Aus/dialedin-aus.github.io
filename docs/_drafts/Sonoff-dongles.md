---
layout: post
title:  "Setup the Sonoff Dongles on Home Assistant with ZHA"
date:   2023-01-27 13:38:43 +1000
last_modified_at: 2023-01-26 22:01:21 +1100
description: Adding the Sonoff ZBDongle-P or ZBDongle-E to your Home Assistant setup, brings support for a wide range of Zigbee devices. Learn all about getting setup here.
featured_image: /assets/img/sections/mark-harrison.jpg
categories: 
  - Home Assitant
---


#### ZBDongle-P Vs ZBDongle-E
quick comparison

#### Zigbee Home Automation
These device should be auto-detected by ZHA

#### Zigbee2MQTT

ZBDongle-P
```
serial:
  port: /dev/ttyUSB0
```


ZBDongle-E
```
serial:
  port: /dev/ttyUSB0
  adapter: ezsp
```



Flash with cc2538-bsl
```
$ ./cc2538-bsl.py -e -w -v -p /dev/ttyUSB0 --bootloader-sonoff-usb ./CC1352P2_CC2652P_launchpad_coordinator_20220219.hex
```

```
$ ./cc2538-bsl.py -e -w -v -p /dev/ttyUSB0 --bootloader-sonoff-usb ./CC1352P2_CC2652P_launchpad_coordinator_20220219.hex 
sonoff
Opening port /dev/ttyUSB0, baud 500000
Reading data from ./CC1352P2_CC2652P_launchpad_coordinator_20220219.hex
Your firmware looks like an Intel Hex file
Connecting to target...
CC1350 PG2.0 (7x7mm): 352KB Flash, 20KB SRAM, CCFG.BL_CONFIG at 0x00057FD8
Primary IEEE Address: 00:12:4B:00:25:8D:44:A8
    Performing mass erase
Erasing all main bank flash sectors
    Erase done
Writing 360448 bytes starting at address 0x00000000
Write 104 bytes at 0x00057F988
    Write done                                
Verifying by comparing CRC32 calculations.
    Verified (match: 0xddfc152d)
```