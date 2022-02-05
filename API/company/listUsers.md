---
layout: default
title: List emplyees
nav_order: 7
parent : Company
grand_parent : API
---

# List users
List all users in a company where the user is Administrator.


### Request
You need to send a GET request with the following style example 
```
https://api.atjek.com/company/listUsers/:userID
```

the GET request needs to have your userID.

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `userID`               | Number            | Yes        | User ID for the user you want a employee list from |

### Response
You will get a response object with a list of company and users assosiated with all companies.

| Field              | Type              | Description  |
|--------------------|-------------------|--------------|
| `companyList`      | Array Object      | Company and company details | 
| `companyUser`      | Array Object      | Company users assosiated with your companies |

### Example input
```
```

### Example response
```
{
    "companyList": [
        {
            "id": 1,
            "companyName": "Electrical installation",
            "ownerAdminUserID": 48,
            "companyAdressStreetName": "Road name ",
            "companyAdressStreetNumber": "123",
            "companyAdressPostalCode": "8000",
            "companyAdressCity": "City Name",
            "companyCountryID": 103
        },
    ],
    "companyUser": [
        {
            "id": 1,
            "companyID": 1,
            "userID": 48,
            "approved": 1,
            "deleted": 0,
            "email": "myname@email.com",
            "firstname": "Ronald",
            "lastname": "Hansen",
            "phone": "755 00 000",
            "mobile": "+47 677 77 988",
            "jobtitle": "Project leader"
        }
    ]
}
```

