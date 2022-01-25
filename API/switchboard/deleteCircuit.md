---
layout: default
title: Delete circuit
nav_order: 7
parent : Switchboard
grand_parent : API
---

# List options
This will delete a circuit to a switchboard spesified in the parameters. 

### Request
You need to send a POST request with the following style example 
```
https://api.atjek.com/switchboard/deleteCircuit
```

You can only delete a circuit from a switchboard you have access to. If you don`t have access to a switchboard you will get an error message. 
Please make sure you first have access to a switchboard by requesting a view from the API.

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `circuitNumber`        | Number            | Yes        | Circuit ID of the circuit you want to delete. |

### Response
You will get a response `Object` with the following data:

| Field              | Type              | Description  |
|--------------------|-------------------|--------------|
|       |       | | 

### Example response
```
```