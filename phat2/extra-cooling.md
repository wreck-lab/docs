---
layout: default
parent: Extra
grand_parent: printHAT 2 Manual
title: Cooling
nav_order: 1
has_children: false
---

# Cooling options

Keeping the printHAT 2 cool during operations allows for more reliable print runs, increased performance of the electronics and ultimately longer life of the control board.  

Properly dissipating the heat is even more critical when the printHAT 2 is coupled to a Rasperry Pi 4 since that board runs particularly hot and its heat adds up to the one of the printHAT 2, mostly dominated by the stepper drivers load.

Depending on the performance requirements and the installation constraints on your machine, you can choose one of the options described in the next sections.  
The table provides the suggested cooling option based on the configured stepper motor running current.

| Convection  | Heatsinks | Heatsinks + Forced cooling |
|:-------------------------:|:-------:|:-------:|
| up to **0.8A** | up to **0.8A** | up to **1.5A** |

## Natural convection
Natural convection is an effective way of cooling the board especially on machines that do not require high stepper motor current (small machines, low accelerations).

It is recommended to install the board vertically, with one of its longer sides facing down. In this way both top and bottom faces of the board will get the best cooling possible (warm air can always move upwards compared to the board laying flat where the bottom side is poorly cooled).    

## Heatsinks
The installation of the heatsinks (provided with the board) can improve the cooling of some fan-less setups.

Since the installation still relies on natural convection the same considerations about the installation described before are applicable.
The heatsinks shall be installed with their fins and channels oriented vertically to facilitate the upwards flow of the hot air and improve cooling.

![forced-cooling](../assets/img/phat2_heatsinks.png)

## Forced cooling
The most effective cooling is achieved using heatsinks and a fan to force the airflow in-between the printHAT 2 and the Raspberry Pi stack.
The airflow will carry away most of the heat right from where it is generated, in the area under the stepper drivers on the bottom side of the board.

The orientation of the board is less critical with forced cooling than with natural convection, however it's always better to install the board vertically, on the long side, as described before.

The fan shall be installed such that the flow direction is upwards.  
