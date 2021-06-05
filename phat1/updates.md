---
layout: default
parent: printHAT 1 Manual
title: Updates
nav_order: 9
---

## WrecklabOS release
This method consists of downloading a wrecklabOS image file and prepare a new SD card.

TODO : missing the steps on how to flash the MCU

## Update script
This method consists of running the wrecklab update script.

TODO : add steps on how to run the script




## Update via wrecklabOS image
Before flashing the new image, you should save your configuration file. Using the OctoKlipper interface copy the content and save it on your PC to be able to restore it later. The software can be updated by flashing the SD card with latest image and following the steps described in the [Initialize the board](initialize) section of this manual.

## Update via Klipper repository
If you wish to update the software by pulling the latest version from the Klipper repository, be aware that there might regressions or bugs which could affect, or even damage, the board.

The Klipper repository in the Wrecklab image points directly at the official Klipper repository. Therefore, it is sufficient to follow these steps:

1. Use SSH to connect to your Raspberry Pi
2. Login with the standard Raspberry Pi credentials: *username: pi, password: raspberry*
3. Navigate to the Klipper folder
4. Pull the latest version: *git pull*
5. Create the firstrun file: *sudo touch /boot/firstrun*

At this point you already have the latest version of Klipper and you just need to reflash the microcontroller.
It is sufficient to shut the printer down and follow the steps described in the [Initialize the board](initialize) section.
