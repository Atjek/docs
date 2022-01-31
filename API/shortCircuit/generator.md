---
layout: default
title: Generator
nav_order: 6
parent : Short circuit
grand_parent : API
---

# Switchboard
Will do a short circuit calculation of one transformer

### Request
You need to send a POST request with the following style example 
```
https://api.atjek.com/shortCircuit/generator/calculate
```

### parameters 

| Parameter              | Type              | Required ? | Description                      |
|------------------------|-------------------|------------|----------------------------------|
| `voltage`              | Number            | Yes        | Generator voltage                |
| `sn`                   | Number            | Yes        | Generator power                  |
| `xdPU`                 | Number            | Yes        | readtance Per Unit               |
| `xdTransPU`            | Number            | Yes        | reactance transient per unit     |
| `xdSubPU`              | Number            | Yes        | reactance sub transient per unit |
| `zn`                   | Number            | Yes        | impedance of generator           |

### Response
The response wil be a `generator` object with short circuit calculations for a generator.

| Field              | Type              | Description  |
|--------------------|-------------------|--------------|
| `zn`               | Object            |              |
| `xdSub`            | Object            |              |
| `xdTrans`          | Object            |              |
| `xd`               | Objet             |              |
| `ik3pmaxSub`       | Object            |              |
| `ik3pmaxTrans`     | Object            |              |
| `ik3pmax`          | Object            |              |
| `iShock`           | Object            |              |

### Example input
```
{
  "voltage": 230,
  "sn": 1000,
  "xdPU": 1.15,
  "xdTransPU": 0.2,
  "xdSubPU": 0.25,
  "zn": 0.4
}
```

### Example response
```
{
  "voltage": 230,
  "sn": 1000,
  "xdPU": 1.15,
  "xdTransPU": 0.2,
  "xdSubPU": 0.25,
  "zn": {
    "value": 0.0529,
    "formula": "ZN = { 230^2 \\over 1000 \\cdot 10^3}",
    "formula_raw": "ZN = { Un^2 \\over Sn}",
    "unit": "&#8486;"
  },
  "ikmaxToIkMin": 1.24,
  "cFactor": 0.95,
  "cFactorMax": 1.05,
  "numDesimals": 2,
  "xdSub": {
    "value": 0.013225,
    "formula": "xd' = { 0.25 \\cdot 0.05 \\Omega }",
    "formula_raw": "xd' = { xd'' \\cdot zn}",
    "unit": "&#8486;"
  },
  "xdTrans": {
    "value": 0.01058,
    "formula": "xd'' = { 0.2 \\cdot 0.05 \\Omega }",
    "formula_raw": "xd'' = { xd'' \\cdot zn}",
    "unit": "&#8486;"
  },
  "xd": {
    "value": 0.060835,
    "formula": "xd = { 1.15 \\cdot 0.05 \\Omega}",
    "formula_raw": "xd = { xd \\cdot zn}",
    "unit": "&#8486;"
  },
  "ik3pmaxSub": {
    "value": 0.0017561551813075444,
    "formula": "Ik'' = { 230 V \\over \\sqrt{3} \\cdot 0.01 \\Omega \\cdot 10^-3 }",
    "formula_raw": "Ik'' = { Un \\over \\sqrt{3} \\cdot Xd'' }",
    "unit": " kA"
  },
  "ik3pmaxTrans": {
    "value": 0.0014049241450460356,
    "formula": "Ik' = { 230 V \\over \\sqrt{3} \\cdot 0.01 \\Omega \\cdot 10^-3}",
    "formula_raw": "Ik' = { Un \\over \\sqrt {3} \\cdot Xd' }",
    "unit": " kA"
  },
  "ik3pmax": {
    "value": 0.008078313834014705,
    "formula": " Ik = { 230 V \\over \\sqrt{3} \\cdot 0.06 \\Omega \\cdot 10^-3 }",
    "formula_raw": "Ik = { Un \\over \\sqrt {3} \\cdot Xd }",
    "unit": " kA"
  },
  "iShock": {
    "value": 0.004390387953268861,
    "formula": "Is = {2.5 \\cdot 0.00 kA }",
    "formula_raw": "Is = { 2,5 \\cdot Ik''}",
    "unit": " kA"
  }
}
```