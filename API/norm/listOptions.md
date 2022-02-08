---
layout: default
title: List options
nav_order: 2
parent : Norm
grand_parent : API
---

# List Options
This will get you a list of options that normaly applies from norms you have selected.

### Request
You need to send a POST request with the following style example 
```
https://api.atjek.com/norm/listOptions
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
| `cableRefInstMet`  | Array object      | Object array of cable installation methods. | 

### Example response
```
{
    "cableRefInstMet": [
        [
            {
                "text": "Cable Ref. inst Met:",
                "value": null
            },
            {
                "text": "A1 - One core hidden",
                "shortName": "A1",
                "value": 1
            },
            {
                "text": "A2 - Multiple core hidden",
                "shortName": "A2",
                "value": 2
            },
            {
                "text": "B1 - One core in tube (canal), open",
                "shortName": "B1",
                "value": 3
            },
            {
                "text": "B2 - Multiple core in tube (canal) open",
                "shortName": "B2",
                "value": 4
            },
            {
                "text": "C - Open",
                "shortName": "C",
                "value": 5
            },
            {
                "text": "D1 - Cable in tube in ground",
                "shortName": "D1",
                "value": 6
            },
            {
                "text": "D2 - Cable direct in ground",
                "shortName": "D2",
                "value": 7
            },
            {
                "text": "E - Multiple core in air (and cable ladder)",
                "shortName": "E",
                "value": 8
            },
            {
                "text": "F - One core in air, close",
                "shortName": "F",
                "value": 9
            },
            {
                "text": "G - One core in air, spred",
                "shortName": "G",
                "value": 10
            },
            {
                "text": "S - Bus bar",
                "shortName": "S",
                "value": 11
            }
        ]
    ]
}
```