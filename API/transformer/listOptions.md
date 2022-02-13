---
layout: default
title: List options
nav_order: 2
parent : Transformer
grand_parent : API
---

# List Options
This will get you a list off all options you can sort a transformer from. This is used in sorting from the frontend. 
You can also use it to get a list of all types of brands, types, and coupling types in the Atjek database.

### Request
You need to send a GET request with the following style example 
```
https://api.atjek.com/transformer/listOptions
```

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
|                        |                   |            |              |

No input parameters available

### Response
You will get a response `Object` with the following data:

| Field                 | Type              | Description  |
|-----------------------|-------------------|--------------|
| `transformerProducer` | Array object      | Object array of available transformer producers with ID and name.  | 
| `transformerType`     | Array object      | Object array of types from producers.                              |
| `transformerCoupling` | Array object      | Object array of available transformer coupling types               |
| `transformerfrequency`| Array object      | Object array of available transformer frequency                    | 

### Example response
```
{
    "transformerProducer": [
        {
            "id": 2,
            "name": "Møre trafo"
        },
        {
            "id": 1,
            "name": "Noratel"
        }
    ],
    "transformerType": [
        {
            "id": 1,
            "name": "3LT-23"
        }
    ],
    "transformerCoupling": [
        {
            "id": 1,
            "name": "Dyn11"
        }
    ],
    "transformerfrequency": [
        {
            "frequency": 50,
            "COUNT(frequency)": 1
        },
        {
            "frequency": 60,
            "COUNT(frequency)": 1
        }
    ]
}
```