---
layout: default
parent: Configure printer
grand_parent: printHAT 2 Manual
title: Cartesian
nav_order: 1
has_children: false
---

## Cartesian printer
The **[stepper]** sections requires the following parameters to be set:

- **step_distance**: defines the length in mm of a single step. If you are unsure check the [Klipper FAQ](https://github.com/KevinOConnor/klipper/blob/master/docs/FAQ.md#how-do-i-calculate-the-step_distance-parameter-in-the-printer-config-file)
- **position_endstop**: Location of the endstop (in mm)
- **position_max**: Maximum valid distance (in mm) the user may command the stepper to move to
- **dir_pin**: Specifies the stepper direction. The direction can be inverted adding “!” in front of the pin name. For instance, stepper_x is inverted by configuring the dir_pin to !PA6

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

The **[printer]** section that you will find in your configuration file if you have selected the cartesian file. The default values should work on every machine, but can very well be adjusted:
- **max_velocity**, **max_accel**: define the performance of the X and Y moves (in mm/s and mm/s2)
- **max_z_velocity**, **max_z_accel**: define the performance of the Z moves (in mm/s and mm/s2)

``` py
[printer]
kinematics: cartesian
max_velocity: 500
max_accel: 1000
max_z_velocity: 25
max_z_accel: 30
```
