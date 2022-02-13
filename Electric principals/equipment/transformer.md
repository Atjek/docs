---
layout: default
title: Transformer
nav_order: 3
parent : Equipment types
grand_parent : Electrical principals
---

# Fuse

## Overview
An transformer is an electrical device used to change the voltage from one level to antoher. It can also be used as an isolater to prevent fault current to the rest of the electrical network.


## Transformer object

| Parameter              | Description                      |  Example                   | Info                          |
|------------------------|-------------------               |----------------------------|-------------------------------|
| `producer`             | Producer name                    | Noratel                    | Se transformer_producer table |
| `type`                 | Producer type                    | 3LT-23                     | Se transformer_model table    |
| `model`                | Transformer model                | 3LT 40.0                   | Se transformer table          |
| `phase`                | 1-phase, split phase, 3 phase    | 3 phase                    | 1 = 3 phase, 2 = split, 3 = 3 phase |
| `frequency`            | transformer operation frequency  | 50                         | Hz                            |
| `primary_voltage_min`  | Tranformer primary min voltage   | 115V                       | Volt                          |
| `primary_voltage_max`  | Transformer primary max voltage  | 1000V                      | Volt                          |
| `secondary_voltage_min`| secondary side min voltage       | 115V                       | Volt                          |
| `secondary_voltage_max`| Secondary side max voltage       | 1000V                      | Volt                          |
| `amp_primary`          | Ampere in 100% load primary      | 1000A                      | Ampere (Calculated)           |
| `amp_secondary`        | Ampere in 100% load secondary    | 57A                        | Ampere (Calculated)           |
| `kva`                  |                                  |                            | KVA                           |
| `coupling_group`       | Transformer coupling group       | Dyn11                      | Se `transformer_coupling` table and reference to `transformer_coupling_group` table for a list of all group transformer can be connected to.|
| `isolation_class`      | Transformer isolation class      | 1                          | 1 = normal 2 = double isolated|
| `ex`                   |                                  |                            |                               |
| `er`                   |                                  |                            |                               |
| `ek`                   |                                  |                            |                               |
| `x0`                   |                                  |                            |                               |
| `r0`                   |                                  |                            |                               |
| `ic`                   | Ic peak                          |                            |                               |
| `n1_n2`                | Turns ratio                      | 1,73                       | 1.73 more vinding on primary vinding. Primary / secondary vinding |
 
