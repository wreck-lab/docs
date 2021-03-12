---
layout: default
title: Setup Wi-fi
nav_order: 3
has_children: false
permalink: /phat_v1_manual/setup_wifi/
has_toc: true
---

If you would like to configure the Raspberry PI to connect to your wi-fi, this is the right time to do it.

Etcher automatically disconnect the media after it's been flashed, therefore you should disconnect and reconnect the SD card reader and then do the following:

1. Open the removable drive named "boot"
2. Open the file "octopi-wpa-supplicant.txt" with a text editor
3. Replace YOURSSID with the name of your wi-fi network
4. Replace YOURPASSWORD with your wi-fi password
5. Make sure the lines are uncommented  (remove the '#' symbol in front) as shown in the picture

``` bash
## WPA/WPA2 secured
network = {
  ssid="put SSID here"
  psk="put password here"
}
```
