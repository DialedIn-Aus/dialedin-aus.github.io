---
layout: post
title:  "5 Must-Have Home Assistant Add-ons: Extended Device & Automation Support (Part 2)"
date:   2023-04-25 10:14:37 +1000
last_modified_at: 2023-04-25 10:14:37 +1000
description: Discover the best Home Assistant add-ons that will take your automation game to the next level. Learn about ESPHome for custom devices, Zigbee2MQTT for improved Zigbee support, NodeRed for powerful automations, Matter for next-gen devices and TasmoAdmin to manage all your Tasmota devices. Boost your experience working with Home Assistant using these must-have add-ons.
featured_image: /assets/img/sections/thomas.jpg
categories: 
  - Home Assistant
---
Home Assistant is an open-source home automation platform that enables users to control and automate various smart devices in their homes. One of the significant advantages of Home Assistant is its extensibility through the use of add-ons, which can be added to the platform to expand its functionality. In a [previous blog post]({% post_url 2023-01-28-5-best-home-assistant-add-ons %}), we shared the five best add-ons for improving your experience working with Home Assistant and making working with configuration files and automations more accessible. In this blog post, we will be discussing the top five add-ons that can help users supercharge their automations and expand device support for Home Assistant. The add-ons we'll be covering in this blog post are ESPHome, Zigbee2MQTT, NodeRed, Matter, and TasmoAdmin.

### 1. ESPHome:

ESPHome is a powerful extension that allows users to create custom firmware for ESP8266/ESP32-based devices. It provides a code-free experience for integrating a [range of development kits](https://shop.dialedin.com.au/collections/development-kits), [sensors, displays](https://shop.dialedin.com.au/collections/sensors) and more.  ESPHome is easy to use and allows users to create a custom firmware using a YAML configuration file without any programming. For the more technical users it also includes an incredibly powerful on-board automation system, that can run entirely independant of any WiFi connection.

This extension adds the ESPHome Dashboard to Home Assistant and is ideal for users who want to create custom devices or modify existing ones (there are some commercially available devices running ESPHome).

You can find more information and installation instructions for the ESPHome here: [https://esphome.io/guides/getting_started_hassio.html](https://esphome.io/guides/getting_started_hassio.html)

### Zigbee2MQTT:

Zigbee2MQTT is an alternative Zigbee stack that allows users to integrate [Zigbee devices](https://shop.dialedin.com.au/collections/zigbee-devices) into Home Assistant. Zigbee2MQTT works by connecting with a [Zigbee dongle](https://shop.dialedin.com.au/collections/zigbee-gateways) then bridging the Zigbee network to Home Assistant. While Home Assistant includes Zigbee Home Automation (ZHA) by default, this add-on is favoured by many advanced Home Assistant users. This extension is useful for users who want to use Zigbee devices that are not supported by ZHA, wish to control Zigbee devices with MQTT or just have more control over configuration of your Zigbee network.  

You can find more information and installation instructions for the Zigbee2MQTT here: [https://github.com/zigbee2mqtt/hassio-zigbee2mqtt#installation](https://github.com/zigbee2mqtt/hassio-zigbee2mqtt#installation)

### NodeRed:

NodeRed is an extension that allows users to create complex automations and flows in Home Assistant. It greatly expands the capabilities of what can be done in automations compared to the builtin automations. NodeRed uses a drag-and-drop graphical interface, making it easy to create automations without writing any code. This extension is ideal for users who want to create advanced custom automations for their smart home.  

You can find more information and installation instructions for the NodeRed add-on here: [https://github.com/hassio-addons/addon-node-red/blob/main/node-red/DOCS.md](https://github.com/hassio-addons/addon-node-red/blob/main/node-red/DOCS.md)

### Matter:

Matter is an upcoming smart home standard that aims to make smart home devices more interoperable. Home Assistant has already added experimental support for Matter, making it easy for users to integrate Matter devices into their smart homes. Matter is still in development, but it is expected to become more popular as more devices support it. As it matures expect this add-on to become a core component of Home Assistant, but for now get ahead of the tech and start experimenting with Matter today.  

[https://www.home-assistant.io/integrations/matter](https://www.home-assistant.io/integrations/matter/)

### TasmoAdmin:

Tasmota is an open-source firmware that can be installed on various smart devices, such as smart switches and bulbs that are based on Espressif ESP32 microcontroller. It provides a core Operating system that is not dependant on any proprietry smart phone apps or cloud connections. Tasmota is natively supported by Home Assistant, providing a seamless connection for your automations to control these devices.

TasmoAdmin is an add-on that allows users to manage and configure Tasmota-based devices from Home Assistant UI. TasmoAdmin makes it easy to configure Tasmota devices and adds integrated support for mangaging device updates into Home Assistant.  If you have multiple Tasmota devices, this makes managing updates a dream.

You can find more information and installation instructions for the TasmoAdmin add-on here: [https://github.com/hassio-addons/addon-tasmoadmin/blob/main/tasmoadmin/DOCS.md](https://github.com/hassio-addons/addon-tasmoadmin/blob/main/tasmoadmin/DOCS.md)

#### Want to try out any of these extensions?
 Installing an add-on in Home Assistant is a relatively simple process. Here are the general steps to follow:

1. Log in to your Home Assistant instance.
2. Go to the menu and select "Settings".
3. In the settings menu, select "Add-ons"
4. From there you will be able to see all the add-ons that are installed on your system. 
5. Click the "Add-on Store" button. You can now search for the add-on you want to install in the search bar or browse the available add-ons. Some addon require adding a third part repository first, see the docs for your addon if this is required.
6. Once you find the add-on, select it and then click on the "Install" button.
7. Wait for the installation process to complete. This may take a few minutes, depending on the add-on and the speed of your internet connection.
8. Before starting the add-on, it's important to read the documentation tab to understand how the add-on works and what configurations it needs. The documentation tab will provide you with more information on how to configure the add-on and how to use it.
9. Once you have read the documentation, you can start the add-on by clicking the "Start" button.

#### Conclusion
Home Assistant is a powerful open-source home automation platform that can be further enhanced with a large selection of add-ons. In this article, we have highlighted the top five add-ons that can supercharge automations and expand device support for Home Assistant. ESPHome allows users to create custom firmware for ESP8266/ESP32-based devices, Zigbee2MQTT adss Zigbee to Home Assistant for advanced control over Zigbee devices, NodeRed provides a graphical interface for creating complex automations, Matter offers experimental support for the upcoming smart home standard, and TasmoAdmin makes managing and configuring Tasmota-based devices seamless within Home Assistant. These add-ons provide enhanced functionality, flexibility, and interoperability to Home Assistant, allowing users to create a more customised and powerful smart home automation system. Whether you're a DIY enthusiast or a smart home power user, these add-ons can help you take your Home Assistant setup to the next level.