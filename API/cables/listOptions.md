---
layout: default
title: List options
nav_order: 3
parent : Cables
grand_parent : API
---

# List Options
This will get you a list off all options you can sort a cable from. This is used in sorting from the frontend. 
You can also use it to get a list of all types of isolations, cabletypes, cablesizes and cablematerials in the Atjek database.


### Request
You need to send a GET request with the following style example 
```
https://api.atjek.com/cables/listOptions
```

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| | | |

No input parameters available

### Response
You will get a response `Object` with the following data:

| Field              | Type              | Description  |
|--------------------|-------------------|--------------|
| `cableBrand`       | Array object      | Object array of available cablebrands with ID and name | 
| `cableFireClass`   | Array object      | Object array of available cable fireclassed with ID and name |
| `cableIsolation`   | Array object      | Object array of available cable Isolation type with ID and name |
| `cableType`        | Array object      | Object array of available cable types with ID and name |
| `cableSize`        | Array object      | Object array of available cable sizeed with ID and name |
| `cableMaterial`    | Array object      | Object array of available cable materiald with ID and name |

### Example response
```
{
    "cableBrand": [
        {
            "id": 1,
            "name": "Draka"
        },
        {
            "id": 2,
            "name": "Nexans"
        },
        {
            "id": 3,
            "name": "Standard"
        }
    ],
    "cableFireClass": [
        {
            "id": 1,
            "fireClass": "Cca"
        },
        {
            "id": 2,
            "fireClass": "Eca"
        },
        {
            "id": 3,
            "fireClass": "Dca"
        }
    ],
    "cableIsolation": [
        {
            "id": 1,
            "cableIsolation": "PVC"
        },
        {
            "id": 2,
            "cableIsolation": "PEX/EPR"
        },
        {
            "id": 3,
            "cableIsolation": "Mineral"
        },
        {
            "id": 4,
            "cableIsolation": "APR"
        }
    ],
    "cableType": [
        {
            "id": 1,
            "cableName": "PFXP"
        },
        {
            "id": 2,
            "cableName": "PR"
        },
        {
            "id": 3,
            "cableName": "PN"
        },
        {
            "id": 4,
            "cableName": "PFSP"
        }
    ],
    "cableSize": [
        {
            "id": 10,
            "cableSize": 0.5
        },
        {
            "id": 11,
            "cableSize": 0.75
        },
        {
            "id": 12,
            "cableSize": 1
        },
        {
            "id": 13,
            "cableSize": 1.5
        },
        {
            "id": 14,
            "cableSize": 2.5
        },
        {
            "id": 15,
            "cableSize": 4
        },
        {
            "id": 16,
            "cableSize": 6
        },
        {
            "id": 17,
            "cableSize": 10
        },
        {
            "id": 18,
            "cableSize": 16
        },
        {
            "id": 19,
            "cableSize": 25
        },
        {
            "id": 20,
            "cableSize": 35
        },
        {
            "id": 21,
            "cableSize": 50
        },
        {
            "id": 22,
            "cableSize": 70
        },
        {
            "id": 23,
            "cableSize": 95
        },
        {
            "id": 24,
            "cableSize": 120
        },
        {
            "id": 25,
            "cableSize": 150
        },
        {
            "id": 26,
            "cableSize": 185
        },
        {
            "id": 27,
            "cableSize": 240
        },
        {
            "id": 28,
            "cableSize": 300
        },
        {
            "id": 29,
            "cableSize": 630
        }
    ],
    "cableMaterial": [
        {
            "id": 1,
            "material": "CU"
        },
        {
            "id": 2,
            "material": "AL"
        }
    ]
}
```