---
layout: default
parent: printHAT 1 Manual
title: Updates
nav_order: 9
---
This page lists the possible ways to keep your system up to date with the latest software developments of the printHAT 1 ecosystem.

## Update via wrecklabOS release
This method consists of downloading a full [wrecklabOS release](https://github.com/wreck-lab/wrecklabOS/releases) file and prepare a new SD card.  
The software contained in the image is tested by our team and represent the most reliable source to get a full update of host, firmware and scripts.  
To update, flash the SD card with latest image and follow the steps described in the [Initialize the board](initialize) section of this manual.

> **IMPORTANT**  
Remember to save your printer configuration file to bring it to the new system. You can use the OctoKlipper interface to copy the configuration and save it on your PC to restore it later.

## Update via Klipper repository (EXPERT USER)
You can update the system to the latest Klipper without reinstalling the full wrecklabOS, pulling the latest version from the Klipper repository.

> **DISCLAIMER**   
Updating to latest Klipper you are installing software that has not been tested by Wrecklab. The software might have regressions or bugs which could affect, or even damage, the board.

The Klipper repository in the Wrecklab image points directly at the official Klipper repository. Therefore, it is sufficient to follow these steps:

1. Use SSH to connect to your Raspberry Pi
2. Login with the standard Raspberry Pi credentials: *username: pi, password: raspberry*
3. Navigate to the Klipper folder
4. Pull the latest version: *git pull*
5. Create the firstrun file: *sudo touch /boot/firstrun*

At this point you already have the latest version of Klipper and you just need to reflash the microcontroller.
It is sufficient to shut the printer down and follow the steps described in the [Initialize the board](initialize) section.
