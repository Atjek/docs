---
layout: default
title: Approve user
nav_order: 7
parent : Company
grand_parent : API
---

# Approve user
Will approve a user who has requested to be added to a company. You need to be an company administrator to be able to approve a user. 


### Request
You need to send a POST request with the following style example 
```
https://api.atjek.com/company/approveUser
```

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `userID`               | Number            | Yes        | User ID for the user you want to approve access to. |
| `companyID`            | Number            | Yes        | Company ID you want the user to be accessed to.     |

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

