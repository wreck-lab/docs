---
layout: default
parent: printHAT V2 Manual
title: Connect to OctoPrint
nav_order: 4
has_children: false
---

The printHAT can be connected to your home network via Wi-Fi or LAN. Upon start up, if the Raspberry Pi can't find a network to connect it will generate its own hot-spot.

Tip {: .label .label-yellow }
Install “Bonjour” to be able to easily find your Octoprint instance without having to remember the IP address.
On Linux and Mac OS the Bonjour software is already integrated. Windows users need to download and install it from here. More information can be found at this link.

## Wifi Or Ethernet
If the wi-fi details have been entered in the wpa-supplicant or the Raspberry Pi has been connected with an Ethernet cable, then it can be reached via [http://wrecklab.local/](http://wrecklab.local/)

## Hot-Spot
The Rasperry Pi creates its own hot-spot when it doesn’t find the wi-fi network configured or when there’s no configuration. The 2.4 Ghz wireless network has the following characteristics:

SSID: wrecklab
Password: raspberry

Once you are connected to it you can reach OctoPrint via [http://wrecklab.local/](http://wrecklab.local/)
