---
layout: default
title: Transformer
nav_order: 5
parent : Short circuit
grand_parent : API
---

# Switchboard
Will do a short circuit calculation of one transformer

### Request
You need to send a POST request with the following style example 
```
https://api.atjek.com/shortCircuit/transformer/calculate
```

The parametert should be sendt inside an `transformerData` object.

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `sk`                   | Number            | Yes        | Short circuit power from high voltage side of transformer |
| `HighVoltage`          | Number            | Yes        | Primary voltage                                           |
| `transVoltage`         | Number            | Yes        | Secondary voltage                                         |
| `sn`                   | Number            | Yes        | Power rating                                              |
| `er`                   | Number            | Yes        | |
| `ex`                   | Number            | Yes        | | 
| `ek`                   | Number            | Yes        | |
| `x0`                   | Number            | Yes        | |
| `r0`                   | Number            | Yes        | |

### Response
The response wil be a complete object with all shortCircuit calculations for a transformer..

| Field              | Type              | Description  |
|--------------------|-------------------|--------------|
| `transVal`         | Object            |              |


### Example input
```

```

### Example response
```

```