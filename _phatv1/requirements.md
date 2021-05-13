---
layout: default
title: Requirements
nav_order: 2
has_children: false
#permalink: /phat_v1_manual/requirements/
has_toc: true
---

Make sure to check out our YouTube channel where you can find tutorials to guide you trough the process! Let’s start now, what you need:

- printHAT control board
- Raspberry Pi 0/1/2/3/4 (RPi 2/3/4 are recommended for a smooth user experience)
- micro SD card, at least 8GB

If you use a Raspberry Pi 4, we strongly recommend you use forced air cooling to cool both the Pi and printHAT. We have custom designed an optimized enclosure that you can [download](https://github.com/wreck-lab/printHAT/tree/master/step/enclosures) and 3D print for free.

# Let’s Get Started
Download the SD image from the [official repository](https://github.com/wreck-lab/printHAT/releases) and use [Etcher](https://www.balena.io/etcher/) to flash the image onto the the SD card as recommended in the Raspberry Pi [official documentation](https://www.raspberrypi.org/documentation/installation/installing-images/). In short:

1. Download Etcher and install it
2. Insert your SD card
3. Open Etcher and select from your hard drive the Wrecklab .img file you want to write on the SD card
4. Select your SD card
5. Review your selections and click ‘Flash!’ to begin writing data to the SD card

![etcher](../assets/img/req_etcher.png)
