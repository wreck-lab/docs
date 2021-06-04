---
layout: default
parent: printHAT 2 Manual
title: Connect to OctoPrint
nav_order: 4
has_children: false
---

The printHAT can be connected to your home network via Wi-Fi or LAN. Upon start up if the Raspberry Pi can't find a network to connect, it will generate its own hot-spot.
> We reccomend installing **Bonjour** to be able to easily find your Octoprint instance without having to remember
the IP address.
> On Linux and Mac OS the Bonjour software is already integrated. Windows users need to download
and install it from [here](https://support.apple.com/kb/DL999?locale=en_US&viewlocale=en_US){:target="_blank"}. More information can be found [here](https://community.octoprint.org/t/i-cant-reach-my-octopi-under-octopi-local/210){:target="_blank"}.

## Wifi Or Ethernet
If the wi-fi details have been entered in the wpa-supplicant ([details](https://community.octoprint.org/t/wifi-setup-and-troubleshooting/184)) or the Raspberry Pi has been connected with an Ethernet cable, then it can be reached via [http://wrecklab.local/](http://wrecklab.local/){:target="_blank"}

## Hot-Spot
The Rasperry Pi creates its own hot-spot when it doesn’t find the wi-fi network configured or when there’s no configuration. The wireless network has the following characteristics:

```bash
SSID: wrecklab
Password: raspberry
```

Once you are connected to it you can reach OctoPrint via [http://wrecklab.local/](http://wrecklab.local/){:target="_blank"}
