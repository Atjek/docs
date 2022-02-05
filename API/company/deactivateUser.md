---
layout: default
title: Deactivate user
nav_order: 8
parent : Company
grand_parent : API
---

# Approve user
Will remove a user who has requested to be added to a company. You need to be an company administrator to be able to deactivate a user. 


### Request
You need to send a POST request with the following style example 
```
https://api.atjek.com/company/deactivateUser
```

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `userID`               | Number            | Yes        | User ID for the user you want to deactivate access to. |
| `companyID`            | Number            | Yes        | Company ID you want the user to be deactivated from.   |

### Response
You will get a response object with a `message` object that contains a message about the update.

| Field              | Type              | Description  |
|--------------------|-------------------|--------------|
| `message`          | Object            | Response     | 

### Example input
```
{
    "id" : 48,
    "companyID" : 2
}
```

### Example response
```
{
    'message' : 'OK'
}
```

