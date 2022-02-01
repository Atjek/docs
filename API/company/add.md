---
layout: default
title: Add company
nav_order: 3
parent : Company
grand_parent : API
---

# List options
Add a company of not exist

### Request
You need to send a POST request with the following style example 
```
https://api.atjek.com/company/add

```
The POST request needs to send an `company` object with parameters as described below. 
You need to be logged in/autenticated to add a company. When you add a company, you will be assisiated with this company, and removed from previous assisiated companies. This as one user can only be assosiated with one company at the time.

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `companyName`          | String            | Yes        | Name of company | 
| `ownerAdminUserID`     | Number            | Yes        | user ID for the user who "owns" this company and can manage users and access to it. When adding a new company, you need to pass in your own user ID |
| `companyAdressStreetName` | String         | No         | Adress street number for company |
| `companyAdressPostalCode` | String         | No         | Postal code for company |
| `companyAdressCity`       | String         | No         | Postal city adress      |
| `companyCountryID`        | Number         | Yes        | Country ID for company  |

### Response
You will get a response `company` `Object` with company data you inserted into database. 

| Field              | Type              | Description  |
|--------------------|-------------------|--------------|
| `company`          | Array Object      | Object with all company hits from search. | 

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
    }
}
```

### Example response
```
{
    "company": {
        "id": 3,
        "companyName": "Electrical services",
        "ownerAdminUserID": 2,
        "companyAdressStreetName": "Default street name",
        "companyAdressStreetNumber": "123",
        "companyAdressPostalCode": "8000",
        "companyAdressCity": "CityName",
        "companyCountryID": 22
    }
}
```

