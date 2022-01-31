---
layout: default
title: Calculate from impedance
nav_order: 4
parent : Short circuit
grand_parent : API
---

# Switchboard
Will do a short circuit calculation based on the impedance.

### Request
You need to send a POST request with the following style example 
```
https://api.atjek.com/shortCircuit/net/impedance/
```

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `ziMax`                | Number            | Yes        | Maximum impedanse  |
| `riMax`                | Number            | Yes        | Maximum resistance |
| `R0Max`                | Number            | No         | Maximum resistance neutral, only needed if TN net |
| `xiMax`                | Number            | Yes        | Maximum reactance  |
| `X0max`                | Number            | No         | Maximum reactance neutral, only needed if TN net |
| `ziMin`                | Number            | Yes        | Total minimum impedance  |
| `riMin`                | Number            | Yes        | Total minumum resistance |
| `r0Min`                | Number            | No         | Total minimum reistance neutral, only needed if TN net |
| `xiMin`                | Number            | Yes        | Total minimum reactance |
| `x0Min`                | Number            | No         | Total minimum reactance neutral, only needed if TN net |
| `zPE`                  | Number            | No         | Total impedance in PE. Only needed if IT |
| `rpeCable`             | Number            | No         | Total resistance in PE. Only needed it IT |
| `xpeCable`             | Number            | No         | Total resistance in PE. Only needed it IT |

### Response
The response wil be a shortCircuit object with short circuit calculation including formulas. This include `ik3pmax`, `ik2pMax`, `ik1pMax`, `ik2pMin`,`ik1pMin`, `VoltageUC`, `ij1pMin` 

| Field              | Type              | Description  |
|--------------------|-------------------|--------------|
| `shortCircuit`     | Object            | Object with all shortCircuit calculations |

### Example input
```


```

### Example response
```


```