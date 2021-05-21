---
layout: default
parent: printHAT 1 Manual
title: Initialize the board
nav_order: 3
has_children: false
---

## Initialization of the board

During the first boot the printHAT image takes care of installing all the required software. Connect the printHAT to the Raspberry Pi following the procedure:

1. Connect the board making sure that the printHAT connector is aligned with the right end of the Raspberry Pi header (see picture)
2. Mount the spacers as shown on the picture
3. Mount the jumper on the BOOT pins
4. Power the Raspberry PI via the Micro USB port with a suitable [power supply](https://www.raspberrypi.org/documentation/hardware/raspberrypi/power/README.md){:target="_blank"}
5. The initialization starts automatically and it takes a couple of minutes.
6. Upon completion the Raspberry Pi goes into shutdown and the ACT led stops blinking. Now it’s possible to power off the Raspberry Pi.
7. Remove the BOOT jumper

## Raspberry Pi 4
If you are using a Raspberry Pi 4 you need to reset the microcontroller at boot to make sure it gets programmed correctly.
When you reach step 3 in the list above, proceed as follows:
- Keep the RESET button pressed on the printHAT
- Power the Raspberry Pi via the Micro USB port with a suitable [power supply](https://www.raspberrypi.org/documentation/hardware/raspberrypi/power/README.md){:target="_blank"}
- As soon as the green LED starts blinking, release the RESET button
- After, the initialization process continues as described in step 5 above


![phat1_assembly](../assets/img/phat1_rpi_assembly.png)
*Fig.1 - printHAT 1 and Raspberry Pi stack alignment*

![phat1_assembly](../assets/img/phat1_rpi_assembly_spacers.png)
*Fig.2 - printHAT 1 spacers installation*

![phat1_assembly](../assets/img/phat1_boot_jumper.jpg)
*Fig.3 - printHAT 1 boot jumper location*
