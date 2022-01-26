---
layout: default
title: List options
nav_order: 2
parent : Fuses
grand_parent : API
---

# List Options
Will do a short circuit calculation of a switchboard with multiple incomming supplyes. Eg one og more generators.

### Request
You need to send a GET request with the following style example 
```
https://api.atjek.com/shortCircuit/switchBoard/
```

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `circuits`             | Array object      | Yes        | Array object of the circuit with equipment connected to the circuit in series. |

### Response
You will get a response `Object` with the following data:

| Field              | Type              | Description  |
|--------------------|-------------------|--------------|
|                    |                   |              |

### Example input
```


```

### Example response
```
{
    "fuseBrand": [
        {
            "id": 1,
            "name": "ABB"
        },
        {
            "id": 2,
            "name": "Eaton"
        },
        {
            "id": 3,
            "name": "Schneider"
        }
    ],
    "fuseSize": [
        {
            "id": 1,
            "size": 0.5
        },
        {
            "id": 2,
            "size": 1
        },
        {
            "id": 3,
            "size": 1.6
        },
        {
            "id": 4,
            "size": 2
        },
        {
            "id": 5,
            "size": 3
        },
        {
            "id": 6,
            "size": 4
        },
        {
            "id": 7,
            "size": 6
        },
        {
            "id": 8,
            "size": 8
        },
        {
            "id": 9,
            "size": 10
        },
        {
            "id": 10,
            "size": 13
        },
        {
            "id": 11,
            "size": 15
        },
        {
            "id": 12,
            "size": 16
        },
        {
            "id": 13,
            "size": 20
        },
        {
            "id": 14,
            "size": 25
        },
        {
            "id": 15,
            "size": 32
        },
        {
            "id": 16,
            "size": 40
        },
        {
            "id": 17,
            "size": 50
        },
        {
            "id": 18,
            "size": 56
        },
        {
            "id": 19,
            "size": 63
        },
        {
            "id": 20,
            "size": 80
        },
        {
            "id": 21,
            "size": 125
        },
        {
            "id": 22,
            "size": 160
        },
        {
            "id": 23,
            "size": 180
        },
        {
            "id": 24,
            "size": 200
        },
        {
            "id": 25,
            "size": 225
        },
        {
            "id": 26,
            "size": 250
        },
        {
            "id": 27,
            "size": 320
        },
        {
            "id": 28,
            "size": 400
        }
    ],
    "fuseBrandSeries": [
        {
            "id": 2,
            "name": "FAZ"
        },
        {
            "id": 3,
            "name": "PKPM2"
        },
        {
            "id": 1,
            "name": "S200"
        }
    ],
    "fuseType": [
        {
            "id": 4,
            "name": "Circuit Breaker"
        },
        {
            "id": 3,
            "name": "Fuse (melt)"
        },
        {
            "id": 1,
            "name": "Miniature Circuit Breakers"
        },
        {
            "id": 2,
            "name": "Motor protection"
        }
    ],
    "fuseTypeSub": [
        {
            "id": 1,
            "name": "MCB",
            "parentTypeID": 1
        },
        {
            "id": 2,
            "name": "MCB w/ RCCB",
            "parentTypeID": 1
        },
        {
            "id": 3,
            "name": "Overload",
            "parentTypeID": 1
        }
    ],
    "fuseSwitchLevel": [
        {
            "id": 1,
            "name": "B"
        }
    ]
}
```