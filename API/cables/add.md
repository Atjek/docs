---
layout: default
title: Add
nav_order: 4
parent : Cables
grand_parent : API
---

# Add cable
This will add a new cable to the database

### Request
You need to send a POST request with the following style example 
```
https://api.atjek.com/cables/add
```

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `cableIsolationFilter` | Array             | No         | Array of mySQL table ID of cableIsolation you want to include in return response |


### Response
You will get a response `Object` with the following data: 

| Field              | Type              | Description  |
|--------------------|-------------------|--------------|
| `cables`           | Array Object      | Object array of cable. | 

### Example response