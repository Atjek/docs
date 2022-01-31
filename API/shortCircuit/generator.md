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

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `voltage`              | Number            | Yes        | Generator voltage |
| `sn`                   | Number            | Yes        | Generator power |
| `xdPU`                 | Number            | Yes        | readtance Per Unit|
| `xdTransPU`            | Number            | Yes        | reactance transient per unit |
| `xdSubPU`              | Number            | Yes        | reactance sub transient per unit |
| `zn`                   | Number            | Yes        | impedance of generator|

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

```

### Example response
```

```