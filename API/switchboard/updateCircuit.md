---
layout: default
title: Update circuit
nav_order: 8
parent : Switchboard
grand_parent : API
---

# List options
This will update a circuit to a switchboard spesified in the parameters. 

### Request
You need to send a POST request with the following style example 
```
https://api.atjek.com/switchboard/updateCircuit
```

You can only update a circuit from a switchboard you have access to. If you don`t have access to a switchboard you will get an error message. 
Please make sure you first have access to a switchboard by requesting a view from the API.

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `circuitData`          | Object            | Yes        | A circuit object with data you want to set. You can fetch circuit data first with /switchboard/view/, and then change the parameters you want to the object and then update it. |

### Response
You will get a response `Object` with the following data:

| Field              | Type              | Description  |
|--------------------|-------------------|--------------|
|       |       | | 

### Example response
```
```