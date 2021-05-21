---
layout: default
parent: Configure printer
grand_parent: printHAT 2 Manual
title: CoreXY
nav_order: 3
has_children: false
---

## CoreXY printer
The **[stepper]** sections requires the following parameters to be set:

- **step_distance**: defines the length in mm of a single step. If you are unsure check the [Klipper FAQ](https://github.com/KevinOConnor/klipper/blob/master/docs/FAQ.md#how-do-i-calculate-the-step_distance-parameter-in-the-printer-config-file)
- **position_endstop**: distance (in mm) between the nozzle and the bed when the nozzle is centred and touching the bed
- **dir_pin**: Specifies the stepper direction. The stepper motors direction depends on your printer configuration. The direction can be inverted adding “!” in front of the pin name. For instance, stepper_a is inverted by configuring the dir_pin to !PA6

``` py
[stepper_x]
step_distance: .0125
position_endstop: 0
position_max: 200
dir_pin: !PB5

[stepper_y]
step_distance: .0125
position_endstop: 0
position_max: 200
dir_pin: PA15

[stepper_z]
step_distance: .000625
position_endstop: 0
position_max: 200
dir_pin: !PB12
```  

The **[printer]** section that you will find in your configuration file if you have selected the CoreXY file. The default values should work on every machine, but can very well be adjusted:
- **max_velocity**, **max_accel**: define the performance of the X and Y moves (in mm/s and mm/s2)
- **max_z_velocity**: define the performance of the Z moves (in mm/s)
- **delta_radius**: projection of the diagonal rod onto the XY plane, when the effector is centred (in mm)

``` py
[printer]
kinematics: corexy
max_velocity: 500
max_accel: 1000
max_z_velocity: 25
max_z_accel: 30
```
