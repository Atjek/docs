---
layout: default
title: Equipment
nav_order: 4
parent : Electrical principals
---

# Equipment

## Overview
Equipment is what makes up the cirucuit. Equipment can be connected in series or in parallell. Normaly in Atjek we only support series equipment for now. 

An equipment can be
1. Fuse
2. Cable
3. switch

To be able to check if cable is correcly dimmensionated according to norms we have to store information on how it is installed. This is what maked up most of the equipment data. Also a equipment, mostly cables can be connected to terminals. Therefore this is added in the datatable. 

## Data

| dataType              | description       |
|-----------------------|-------------------|
| equipment_number      | Number of the equipment in series.  If 1 this is the first equipment in the series.                                                   |
| equipmentID           | Equipment ID for the selected equipment. IF the ID is 10, this is a "PR 2x1,5" cable, but and also a Eaton PKM2 fuse. The equipmentType determins where we loop up equipment information. |
| deleted               | Set to 1 if equipment is deleted                                                                                                      |
| switchboardCircuitID  | ID of the circuit the equipment is connected to.                                                                                      |
| equipmentType         | Type of equipment Fuse/cable/switch.                                                                                                  |
| terminalName          | Terminal name if equipment is connected to a terminal. Normaly X1, X2, and so on.                                                     |
| terminalNumber        | Number of the terminal the equipment is connected to if any.                                                                          |
| cableRefInstMet       | Cable ref installation methos according to norm. Set to a number, witch correlated to the index of the table in norm.                 | 
| cableLength           | Length of cable. Used for calculating total R anx X values for circuit.                                                               |
| cableCorFac           | 0-1, factor for decreasing or increasing current carrying capabilities depentent on how many cables around.                           |
| cableTempCor          | 0-1, factor for decreasing or increasing current carrying capabilities depentent on temperature around cables.                        |
| cableOrientation      | If cables is mounted vertical og horisontaly.                                                                                         |
| cableDeltaFormation   | |