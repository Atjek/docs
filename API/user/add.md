---
layout: default
title: Add user
nav_order: 2
parent : User
grand_parent : API
---

# Add user
Add a user to the Atjek database.

### Request
You need to send a POST request with the following style example 
```
https://api.atjek.com/user/add/
```

The POST request needs to send an object with parameters as described below. 

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `email`                | String            | Yes        | Email adress for user |
| `userName`             | String            | Yes        | Username with connect user up to cognito database |
| `companyID`            | Number            | Yes        | Company ID the user shall be assosiated with |
| `firstname`            | String            | Yes        | First name    |
| `lastname`             | String            | Yes        | Last name     |
| `phone`                | String            | Yes        | Phone number  |
| `mobile`               | String            | Yes        | Mobile number |
| `jobtitle`             | String            | Yes        | Job title     |

### Response
You will get a response `Object` with mysql affected rows and inserted ID. 

### Example input
```
{
    "email" : "stian@electricalinstall.com",
    "userName" : "8746aff5-d862-46eb-b984-de0", 
    "comapnyID" : 2,
    "firstname" : "Stian",
    "lastname" : "Thomassen",
    "phone" : "75500000",
    "mobile" : "9740000",
    "jobtitle" : "Project leader"
}

```

### Example response
```
{
    "fieldCount": 0,
    "affectedRows": 1,
    "insertId": 49,
    "info": "",
    "serverStatus": 2,
    "warningStatus": 0
}
```

