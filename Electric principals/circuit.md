---
layout: default
title: Circuit
nav_order: 3
parent : Electrical principals
---

# Circuits

## Overview
From a switchboard there is one or more circuit out to consumers or loads. 
The cirucit is build up by equipment connected on series of parallell.

## Data

| dataType              | description       |
|-----------------------|-------------------|
| circuitnumber         | Circuit number inside the switchboard. For a switchboard with 10 circuits, normaly named 1-10 or XF1 -XF10                            |
| circuitName           | Name of current circuit. A description of what is connected. "Kitchen", "dryer", "bedroom"                                            |
| loadType              | Type of load to this circuit. Switchboard/constant/socker/motor. This is important when checking demands against norms.               |
| loadIn                | Load in Amps for load. If socket set to the same as the fuse.                                                                         |
| loadCos               | Cosphi for the load. Normaly only applied on for motors and inductive loads.                                                          |
| loadStartTime         | Used for motors. Used to check motor start up current and time againt fuse.                                                           |
| loadStartIn           | Used for motors. Used to check motor start up current and time againt fuse.                                                           |
| loadDemandFactor      | If load is not constantly on, we can set this factor (0-1) and lower. This allow us to select a smaler incomming fuse for the switchboard |
| loadEfficiency        | Used for motors.                                                                                                                      |
| switchboardID         | ID of switchboard this circuit is connected to.                                                                                       |
| deleted               | Set to 1 if circuit is deleted.                                                                                                       |
| numCores              | Number of cores the load demands. (1-4)                                                                                               |
| normID                | NormID used to check cable size and fuse for circuit. If not selected, will use same as switchboard.                                  |