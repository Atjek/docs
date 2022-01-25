---
layout: default
title: List add fuse small
nav_order: 3
parent : Fuses
grand_parent : API
---

# List add fuse small

This will return a fuse based on input size, type, and switchlevel. Example
If you select 10A, MCB w/ RCCB, type B. you will return fuseObject for an Eaton PKM2-10/2/B/003-A fuse. 

This function is normaly only used in the front end for quickly insering a fuse to a circuit. 

### Request
You need to send a POST request with the following style example 
```
https://api.atjek.com/fuse/listAddFuseSmall
```

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `fuseSizeFilter`       | Number            | Yes        | size ID of fuse you want to add |
| `fuseTypeSubFilter`    | Number            | Yes        | fuseTypeSubFilter ID of fuse you want to add |
| `fuseSwitchLevelFilter`| Number            | Yes        | fuseSwitchLevelFilter ID of fuse you want to add |

### Response
You will get a response `Object` with the following data:

| Field              | Type              | Description  |
|--------------------|-------------------|--------------|
| `listFuseAddSmall` | Array object      | Fuse object of acceptable fuse |


### Example response
```
{
    "listFuseAddSmall": [
        {
            "id": 3,
            "fuseBrandID": 2,
            "fuseTypeID": 1,
            "fuseTypeSubID": 2,
            "fuseSizeID": 9,
            "fuseBrandSeriesID": 3,
            "fuseSwitchLevelID": 1,
            "in": 10,
            "inAdjustable": 0,
            "fuseRCDSizeID": 2,
            "iRCDAdjustable": 0,
            "fuseName": "PKM2-10/2/B/003-A",
            "partnumber": null,
            "elnumber": 1654700,
            "numpoles": 2,
            "fuseBreakTypeID": 1,
            "fuseRCDTypeID": 1,
            "numPolesProtectected": 2,
            "fuseBrand": "Eaton",
            "fuseSize": 10,
            "fuseBrandSeries": "PKPM2",
            "ue": [
                {
                    "max": 253,
                    "min": 196,
                    "type": "AC"
                }
            ],
            "fuseTypeSub": "MCB w/ RCCB",
            "fuseSwitchLevel": "B",
            "60898_icn": 10,
            "60898_ics": 7.5,
            "60947_icu": 0,
            "60947_ics": 0,
            "name": "PKM2 - B",
            "i1": 1.13,
            "i2": 1.39,
            "t2": 3600,
            "i4": 3,
            "i5": 4.8,
            "t5": 0.01,
            "iRCD": "30"
        }
    ]
}
```