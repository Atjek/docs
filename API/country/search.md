---
layout: default
title: Search country
nav_order: 2
parent : Country
grand_parent : API
---

# List options
Make a search of a country from mySQL country table. 

### Request
You need to send a GET request with the following style example 
```
https://api.atjek.com/country/search/:countryname
```

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `countryname`          | String            | Yes        | Country name or part of countryname you are searching for. | 

### Response
You will get a response `country` `Array Object` with country data. 

| Field              | Type              | Description  |
|--------------------|-------------------|--------------|
| `country`          | Array Object      | Object with all country hits from search. | 

### Example response
```
{
    "country": [
        {
            "id": 139,
            "countryName": "Norfolk Island",
            "countryCode": "NF",
            "countryPhoneCode": 672
        },
        {
            "id": 140,
            "countryName": "Northern Mariana Islands",
            "countryCode": "MP",
            "countryPhoneCode": 1670
        },
        {
            "id": 141,
            "countryName": "Norway",
            "countryCode": "NO",
            "countryPhoneCode": 47
        }
    ]
}
```

