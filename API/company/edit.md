---
layout: default
title: Edit company
nav_order: 4
parent : Company
grand_parent : API
---

# Edit company
Edit a existing company. You need to be assosiated with the company to be able to edit details.

### Request
You need to send a POST request with the following style example 
```
https://api.atjek.com/company/edit
```
The POST request needs to send an object with parameters as described below. 
You need to be logged in/autenticated as an company administrator to edit a company. 

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `companyName`          | String            | Yes        | Name of company | 
| `ownerAdminUserID`     | Number            | Yes        | user ID for the user who "owns" this company and can manage users and access to it. When adding a new company, you need to pass in your own user ID |
| `companyAdressStreetName` | String         | No         | Adress street number for company |
| `companyAdressPostalCode` | String         | No         | Postal code for company |
| `companyAdressCity`       | String         | No         | Postal city adress      |
| `companyCountryID`        | Number         | Yes        | Country ID for company  |
| `companyID`               | Number         | Yes        | Company ID              |

### Response
You will get a response object with a `message` object that contains a message about the update.

| Field              | Type              | Description  |
|--------------------|-------------------|--------------|
| `message`          | Object            | Response     | 

### Example input
```
{ 
    "company": {
        "companyName": "Electrical services",
        "ownerAdminUserID": 2,
        "companyAdressStreetName": "Default street name",
        "companyAdressStreetNumber": "123",
        "companyAdressPostalCode": "8000",
        "companyAdressCity": "CityName",
        "companyCountryID": 22
        "companyID": 9
    }
}
```

### Example response
```
{
    'message' : 'OK'
}
```

