---
layout: default
title: List 
nav_order: 3
parent : Transformer
grand_parent : API
---

# List
This will get you a list off all transformer from a set of input parameters (if any set). 

### Request
You need to send a POST request with the following style example 
```
https://api.atjek.com/transformer/list
```

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `countryFilter`        | Array             | No         | Array of MySQL table ID of country ID to filter from.                         |
| `producerFilter`       | Array             | No         | Array of MySQL table ID of producers to filter from.                          |
| `typeFilter`           | Array             | No         | Array of MySQL table ID of country ID to filter from.                         | 
| `IDFilter`             | Array             | No         | Array of mySQL table ID of fuse ID you wan to include in return response. Normaly this is used when we want only to get information from a single transformer |

The parameters needs to be passed inside an `option` object. 

### Response
You will get a response `transformer` `Array Object` list containing all information about an transformer. Se transformer in equipment for more information about data.

### Example response
```
{
    "transformer": [
        {
            "id": 1,
            "producer_id": 1,
            "producer_type": "3LT-23",
            "model": "3LT 0.10",
            "country_id": 141,
            "phase": 3,
            "frequency": 50,
            "primary_voltage_min": 115,
            "primary_voltage_max": 1000,
            "secondary_voltage_min": 115,
            "secondary_voltage_max": 1000,
            "kva": 0.1,
            "isolation_class": 1,
            "ex": 22.8,
            "er": 20.7,
            "ek": 23.8,
            "x0": 0,
            "r0": 0,
            "ic": 44,
            "n1_n2": 1.73,
            "deleted": 0,
            "edit": "2022-02-06T23:00:00.000Z",
            "producer_name": "Noratel"
        },
        {
            "id": 2,
            "producer_id": 1,
            "producer_type": "3LT-23",
            "model": "3LT 0.15",
            "country_id": 141,
            "phase": 3,
            "frequency": 50,
            "primary_voltage_min": 115,
            "primary_voltage_max": 1000,
            "secondary_voltage_min": 115,
            "secondary_voltage_max": 1000,
            "kva": 0.15,
            "isolation_class": 1,
            "ex": 19.8,
            "er": 17.8,
            "ek": 18,
            "x0": 0,
            "r0": 0,
            "ic": 46,
            "n1_n2": 1.73,
            "deleted": 0,
            "edit": "2022-02-06T23:00:00.000Z",
            "producer_name": "Noratel"
        }
    ]
}
```