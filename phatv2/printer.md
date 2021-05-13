---
layout: default
parent: printHAT V2 Manual
title: Configure printer
nav_order: 6
has_children: false
---

## Cartesian printer
The [stepper] sections requires the following parameters to be set:

- step_distance: defines the length in mm of a single step. If you are unsure check the [Klipper FAQ](https://github.com/KevinOConnor/klipper/blob/master/docs/FAQ.md#how-do-i-calculate-the-step_distance-parameter-in-the-printer-config-file)
- position_endstop: Location of the endstop (in mm)
- position_max : Maximum valid distance (in mm) the user may command the stepper to move to
- dir_pin: Specifies the stepper direction. The direction can be inverted adding “!” in front of the pin name. For instance, stepper_a is inverted by configuring the dir_pin to !PA6

``` py
[stepper_x]
step_distance: .0125
position_endstop: 0
position_max: 200
dir_pin: PA6

[stepper_y]
step_distance: .0125
position_endstop: 0
position_max: 200
dir_pin: PA15

[stepper_z]
step_distance: .000625
position_endstop: 0
position_max: 200
dir_pin: PC8
```

The [printer] section that you will find in your configuration file if you have selected the cartesian file. The default values should work on every machine, but can very well be adjusted:
- max_velocity, max_accel: define the performance of the X and Y moves (in mm/s and mm/s2)
- max_z_velocity, max_z_accel: define the performance of the Z moves (in mm/s and mm/s2)

``` py
[printer]
kinematics: cartesian
max_velocity: 500
max_accel: 1000
max_z_velocity: 25
max_z_accel: 30
```

## Delta printer
The [stepper] sections requires the following parameters to be set:

step_distance: defines the length in mm of a single step. If you are unsure check the Klipper FAQ
position_endstop: distance (in mm) between the nozzle and the bed when the nozzle is centred and touching the bed
arm_length: length (in mm) of the diagonal rod that connects this tower to the print head.
dir_pin: Specifies the stepper direction. The stepper motors direction depends on your printer configuration. The direction can be inverted adding “!” in front of the pin name. For instance, stepper_a is inverted by configuring the dir_pin to !PA6

``` py
[stepper_a]
step_distance: .0125
position_endstop: 297.05
arm_length: 333.0
dir_pin: PA6

[stepper_b]
step_distance: .0125
position_endstop: 297.05
arm_length: 333.0
dir_pin: PA15

[stepper_c]
step_distance: .0125
position_endstop: 297.05
arm_length: 333.0
dir_pin: PC8
```  

The [printer] section that you will find in your configuration file if you have selected the Delta file. The default values should work on every machine, but delta_radius shall be updated to the one of your machine.

- max_velocity, max_accel: define the performance of the X and Y moves (in mm/s and mm/s2)
- max_z_velocity: define the performance of the Z moves (in mm/s)
- delta_radius: projection of the diagonal rod onto the XY plane, when the effector is centred (in mm)

``` py
[printer]
kinematics: delta
max_velocity: 300
max_accel: 3000
max_z_velocity: 150

delta_radius: 174.75
```
