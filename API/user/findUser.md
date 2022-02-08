---
layout: default
title: Find user
nav_order: 3
parent : User
grand_parent : API
---

# Find user
Find a user from a uniqe AWS cognito username. This is normaly used to identify user from AWS cognito pool to Atjek database as the Atjek database does not contain any username and passwords for users.

### Request
You need to send a POST request with the following style example 
```
https://api.atjek.com/user/findUser
```

The POST request needs to send an object with parameters as described below. 

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `userName`             | String            | Yes        | Cognito username. |

### Response
You will get a response `Object` with the user details from the user table.

### Example input
```
{
    "userName" : "2q7ldqflcjr00iqn3r1egaa8tn"
}
```

### Example response
```
[
    {
        "id": 47,
        "email": "tmc45802@eoopy.com",
        "userName": "2q7ldqflcjr00iqn3r1egaa8tn",
        "companyID": 0,
        "firstname": "Emiliy",
        "lastname": "Hansen",
        "phone": "75000000",
        "mobile": "98767567",
        "jobtitle": "Electrical planner"
    }
]
```

