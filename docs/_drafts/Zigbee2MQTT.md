---
layout: post
title:  "Setup Zigbee2MQTT"
date:   2023-01-27 13:38:43 +1000
last_modified_at: 2023-01-26 22:01:21 +1100
description: Adding the Sonoff ZBDongle-P or ZBDongle-E to your Home Assistant setup, brings support for a wide range of Zigbee devices. Learn all about getting setup here.
featured_image: /assets/img/sections/mark-harrison.jpg
categories: 
  - Home Assitant
---

#### Zigbee2MQTT

1. Home Assistant Advanced mode
2. install mosquitto + start (default settings)
   Configure Discovered MQTT
3. add Z2M repo
https://github.com/zigbee2mqtt/hassio-zigbee2mqtt
4. Install Z2M
5. Find serial port, configure Z2Mserial port: (no ther settings changes)
ZBDongle-P

### Change your Zigbee Network key
(Optional, but recommended)
Zigbee2MQTT uses a well-known default network key to encrpyt all Zigbee traffic, this is a security risk as anyone within range of your Zigbee network could potentially sniff traffic on your network. It is therefore recommended to change this network key to a random value. It is best to do this before you pair any devices, otherwise you will have to repair all devices after changing it.

Unfortunately this is not as easy as it should be to change the network key when using the Zigbee2MQTT when using the Home Assistant Add-on. This is the best way we have found.

1. From Zigbee2MQTT frontend navigate to `settings` -> `advanced`, scroll down until you find the network key setting and select `GENERATE` from the dropdown then click `Submit`.
2. From the Zigbee2MQTT add-on page restart the add-on, this will generate a random network and then fail with an error.
3. Now use ssh, File Editor Add-on or Studio Code Add-on[^1] to delete the file `/config/zigbee2mqtt/coordinator_backup.json`.
4. Go back to the Zigbee2MQTT Add-on page and restart Zigbee2MQTT again. Check the logs, everything should load correctly this time.

Now you can start pairing devices. Click the "Permit Join" button, then you can pair devices until the timer runs about after 5 minutes.

[^1]: Unless you are running Home Assistant on a system with < 2GB RAM, this is a great extension that allows you use Visual studio code right from within the Home Assistant interface to edit any of the configuration files.


```
serial:
  port: /dev/ttyUSB0
  adapter: znp
```


ZBDongle-E
```
serial:
  adapter: ezsp
```

