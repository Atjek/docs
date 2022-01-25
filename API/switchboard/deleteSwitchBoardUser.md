---
layout: default
title: Delete switchboard user
nav_order: 4
parent : Switchboard
grand_parent : API
---

# List options
This will delete a users access to a switchboard. 

### Request
You need to send a GET request with the following style example 
```
https://api.atjek.com/switchboard/deleteSwitchBoardUser/SWITCHBOARDID/USERID
```

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `switchBoardID`        | Number            | Yes        | switchboardID for the switchboard you want to remove a users access to |
| `userID`               | Number            | Yes        | userID of the user you want to delete acces to switchboard to. |


### Response
You will get a response `Object` with the following data:

| Field              | Type              | Description  |
|--------------------|-------------------|--------------|
|      |     |  | 

### Example response
```

``` 