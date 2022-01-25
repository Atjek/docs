---
layout: default
title: Delete equipment
nav_order: 11
parent : Switchboard
grand_parent : API
---

# List options
This will delete a equipment to a circuit spesified in the parameters. 

### Request
You need to send a POST request with the following style example 
```
https://api.atjek.com/switchboard/deleteEquipment
```

You can only delete a equipment to a circuit connected to a from a switchboard you have access to. If you don`t have access to a switchboard you will get an error message. 
Please make sure you first have access to a switchboard by requesting a view from the API.

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `equipmentID`          | Number            | Yes        | equipment ID for equipment you want to delete. |

### Response
You will get a response `Object` with the following data:

| Field              | Type              | Description  |
|--------------------|-------------------|--------------|
|       |       | | 

### Example response
```

```