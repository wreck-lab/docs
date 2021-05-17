---
layout: default
title: Advanced settings
nav_order: 4
has_children: false
---

The [Klipper Wiki](https://github.com/KevinOConnor/klipper/blob/master/docs/Overview.md){:target="_blank"} is the starting point to learn about all the Klipper functionalities and advanced features.

Here a short list of the most common topics:
- all the extended functionalities are documented in the [config file reference doc](https://www.klipper3d.org/Config_Reference.html){:target="_blank"} and they can be added to the printer configuration file
- the list of Klipper supported [commands and G-CODES](https://github.com/KevinOConnor/klipper/blob/master/docs/G-Codes.md){:target="_blank"}
- the [endstop phase detection](https://github.com/KevinOConnor/klipper/blob/master/docs/Endstop_Phase.md){:target="_blank"} algorithm which greatly improves the accuracy of the end stop switches. This aspect is very critical for Delta printers to achieve consistent first layers
- the [Delta Calibration Procedure](https://github.com/KevinOConnor/klipper/blob/master/docs/Delta_Calibrate.md){:target="_blank"} documentation
- the [Bed Levelling Procedure](https://github.com/KevinOConnor/klipper/blob/master/docs/Bed_Level.md){:target="_blank"} documentation
- the [sensorless homing](https://www.klipper3d.org/TMC_Drivers.html){:target="_blank"} supported by the printHAT. If you are willing to activate it follow the Klipper instructions at the link provided. Not recommend for Delta printers due to the lower accuracy compared to regular end-stop switches.
