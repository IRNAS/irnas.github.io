---
layout: post
title: "Simplified Arduino ADC - ESP8266 (nodemcu lua) communication + WS2812B LEDs"
description: "Introducing a simple method of transferring values from Arduino to ESP8266 and displaying them on the web interface + driving LEDs "
category: 
tags: []
---
{% include JB/setup %}

ESP8266 WiFi modules with very affordable price have become highly popular with hackers and developers around the globe, empowered with the great development of NodeMcu lua firmware, further simplifying the use. While there are a number of example setups on the web, none is very simple and effective in using the serial communication to push a few measurements from a microcontroller or Arduino to the ESP module, drive a number of WS2812B serial LEDs and display the raw values on the web interface. Find the details about this quick and dirty method in the [Github repository](https://github.com/IRNAS/SimpleArduinoESP-Lua) or follow the discussion about this on [ESP8266 forum](http://www.esp8266.com/viewtopic.php?f=19&t=1975)