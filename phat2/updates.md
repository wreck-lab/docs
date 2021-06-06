---
layout: default
parent: printHAT 2 Manual
title: Updates
nav_order: 9
has_children: false
---

This page lists the possible ways to keep your system up to date with the latest software developments of the printHAT 2 ecosystem.

## Update via wrecklabOS release
This method consists of downloading a full [wrecklabOS release](https://github.com/wreck-lab/wrecklabOS/releases) file and prepare a new SD card.  
The software contained in the image is tested by our team and represent the most reliable source to get a full update of host, firmware and scripts.  
To update, flash the SD card with latest image and follow the steps described in the [Initialize the board](initialize) section of this manual.

> **IMPORTANT**  
Remember to save your printer configuration file to bring it to the new system. You can use the OctoKlipper interface to copy the configuration and save it on your PC to restore it later.

## Update via script
You can update the software to the latest supported Klipper without reinstalling the full image but via the wrecklabOS update script, as follow:

1. Use SSH to connect to your Raspberry Pi
2. Login with the standard credentials
```py
username: pi
password: raspberry
```
3. Run the update script and follow the prompts:
```bash
./scripts/update_v2.sh
```
