---
layout: default
parent: printHAT V2 Manual
title: Configure Klipper
nav_order: 5
has_children: false
---

Klipper comes pre-configured for a cartesian printer. The configuration can be changed via the OctoPrint interface as follow:

- connect to OctoPrint via [http://wrecklab.local/](http://wrecklab.local/)
- click the settings button
- click on the “OctoKlipper” plugin
- click on the “Klipper Configuration” Tab

The “printer.cfg” file, where the configuration parameters are stored, can be edited manually or copy/paste the content of one of the available templates.

## Configuration File
The configuration file contains few sections that need to be updated. Some sections are general and are described described below.
Some others are specific to a your 3D printer architecture and are described in the next steps (pick the one that matches your printer type)

## Extruder
The extruder section contains also some basic parameters to be configured:

- step_distance: defines the length in mm of a single step. If you are unsure check the Klipper FAQ
- nozzle_diameter: Diameter of the nozzle orifice (in mm)
- filament_diameter: The nominal diameter of the raw filament (in mm) as it enters the extruder
- sensor_type: Type of sensor – this may be “EPCOS 100K B57560G104F”, “ATC Semitec 104GT-2”, “NTC 100K beta 3950”, “Honeywell 100K 135-104LAG-J01”, “NTC 100K MGB18-104F39050L32”, “AD595”, “PT100″, INA826”, “MAX6675”, “MAX31855”, “MAX31856”, or “MAX31865”

```py
[extruder]
step_distance: .0022
nozzle_diameter: 0.400
filament_diameter: 1.750
sensor_type: ATC Semitec 104GT-2
```

## Heated Bed (optional)
 If your machine have a heated bed, then the following section should be added to your configuration file. Make sure the sensor type matches the temperature sensor you have on your bed.

``` py
[heater_bed]
heater_pin: !PA0
sensor_type: ATC Semitec 104GT-2
sensor_pin: PB0
pullup_resistor: 10000
control: watermark
min_temp: 0
max_temp: 120
```
