---
layout: default
title: Delete employee
nav_order: 6
parent : Company
grand_parent : API
---

# Edit company
Delete an emplyee from a company

### Request
You need to send a POST request with the following style example 
```
https://api.atjek.com/company/deleteEmplyee
```

The POST request needs to send an `employee` object with parameters as described below. 

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `id`                   | Number            | Yes        | User ID for the user to be deleted from the company |
| `companyID`            | Number            | Yes        | companyID the user is to be deleted from            |

### Response
You will get a response object with a `message` object that contains a message about the update.

| Field              | Type              | Description  |
|--------------------|-------------------|--------------|
| `message`          | Object            | Response message | 

### Example input
```
{
    "employee" : {
        "id" : "48",
        "companyID" : "5"
    }
}
```

### Example response
```
{
    'message' : 'OK'
}
```

