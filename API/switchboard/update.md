---
layout: default
title: Update
nav_order: 5
parent : Switchboard
grand_parent : API
---

# List options
This will update the switchboard data with the data you send inn as an switchboard Object.

### Request
You need to send a POST request with the following style example 
```
https://api.atjek.com/switchboard/update
```

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `switchBoard`          | Object Array      | Yes        | A switchboard object with data you want to set. You can fetch switchboard data first with /switchboard/view/, and then change the parameters you want to the object and then update it. |
| `supplyCircuit`        | Object            | No        | If you need to change something for the supply circuit, you can use this API call or circuit update. | 


### Response
You will get a response `Object` with the following data:

| Field              | Type              | Description  |
|--------------------|-------------------|--------------|
|       |       | | 

### Example response
```
```