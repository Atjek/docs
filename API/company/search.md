---
layout: default
title: Search company
nav_order: 2
parent : Company
grand_parent : API
---

# List options
Make a search of a company from mySQL company table. 

### Request
You need to send a GET request with the following style example 
```
https://api.atjek.com/company/search/:companyname
```

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `companyname`          | String            | Yes        | Company name or part of companyname you are searching for. | 

### Response
You will get a response `company` `Array Object` with company data. 

| Field              | Type              | Description  |
|--------------------|-------------------|--------------|
| `company`          | Array Object      | Object with all company hits from search. | 

### Example response
```
{
    "company": [
        {
            "id": 2,
            "companyName": "Electrical services",
            "ownerAdminUserID": 2,
            "companyAdressStreetName": "Default street name",
            "companyAdressStreetNumber": "123",
            "companyAdressPostalCode": "8000",
            "companyAdressCity": "CityName",
            "companyCountryID": 22
        }
    ]
}
```

