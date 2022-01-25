---
layout: default
title: Add equipment
nav_order: 10
parent : Switchboard
grand_parent : API
---

# List options
This will add a equipment to a circuit spesified in the parameters. 

### Request
You need to send a POST request with the following style example 
```
https://api.atjek.com/switchboard/addEquipment
```

You can only update a equipment to a circuit connected to a from a switchboard you have access to. If you don`t have access to a switchboard you will get an error message. 
Please make sure you first have access to a switchboard by requesting a view from the API.

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `equipment`            | Object            | Yes        | A equipment object with data you want to set. |

### Response
You will get a response `Object` with the following data:

| Field              | Type              | Description  |
|--------------------|-------------------|--------------|
|       |       | | 

### Example response
```
```