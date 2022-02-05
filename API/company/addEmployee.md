---
layout: default
title: Add employee
nav_order: 5
parent : Company
grand_parent : API
---

# Edit company
Add an emplyee to an existing company

### Request
You need to send a POST request with the following style example 
```
https://api.atjek.com/company/addEmployee
```

The POST request needs to send an object with parameters as described below. 
The company will get a list of added users, and need to aprove them before the user is added to the list of users.

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `userID`               | Number            | Yes        | User ID for the user to be added to the company |
| `companyID`            | Number            | Yes        | Company ID the user is to be added to.          | 

### Response
You will get a response object with a `message` object that contains a message about the update.

| Field              | Type              | Description  |
|--------------------|-------------------|--------------|
| `message`          | Object            | Response message | 

### Example input
```
{
    "userID" : "48",
    "companyID" : "5"
}
```

### Example response
```
{
    'message' : 'OK'
}
```

