---
layout: default
title: Add circuit
nav_order: 6
parent : Switchboard
grand_parent : API
---

# List options
This will add a circuit to a switchboard spesified in the parameters. 

### Request
You need to send a POST request with the following style example 
```
https://api.atjek.com/switchboard/addCircuit
```

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `circuitData`          | Object            | Yes        | A circuit object containing all nececary circuitData. |
| `switchboardID`        | Number            | Yes        | ID of the switchboard you want to add the circuit to. |
| `equipment`            | Object array      | Yes        | An object array of all equipment connected to this circuit |


### Response
You will get a response `Object` with the following data:

| Field              | Type              | Description  |
|--------------------|-------------------|--------------|
|       |       | | 

### Example response
```
```


          circuitData   : this.circuitData,
          switchboardID : this.switchBoard.id,
          equipment     : equipmentAdd