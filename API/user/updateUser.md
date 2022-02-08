---
layout: default
title: Update user
nav_order: 4
parent : User
grand_parent : API
---

# Find user
Update a user information.

### Request
You need to send a POST request with the following style example 
```
https://api.atjek.com/user/findUser
```

The POST request needs to send a `user` object with parameters as described below. 

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `id`                   | Number            | Yes        | user id      |
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
    "user" :  {
        "id": 47,
        "email": "tmc45802@eoopy.com",
        "userName": "2q7ldqflcjr00iqn3r1egaa8tn",
        "companyID": 0,
        "firstname": "Helene",
        "lastname": "Olsen ",
        "phone": "1234578",
        "mobile": "987654321",
        "jobtitle": "Senior developer"
    }
}
```

### Example response
```
{
    "fieldCount": 0,
    "affectedRows": 1,
    "insertId": 0,
    "info": "Rows matched: 1  Changed: 1  Warnings: 0",
    "serverStatus": 2,
    "warningStatus": 0,
    "changedRows": 1
}
```

