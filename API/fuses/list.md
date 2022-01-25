---
layout: default
title: List 
nav_order: 4
parent : Fuses
grand_parent : API
---

# List
This will get you a list off all fuses from a set of input parameters (if any set). 

### Request
You need to send a POST request with the following style example 
```
https://api.atjek.com/fuse/list
```

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `fuseBrandFilter`      | Array             | No         | Array of mySQL table ID of fuse brands you want to include in return response |
| `fuseSizeFilter`       | Array             | No         | Array of mySQL table ID of fuse sizes you want to include in return response  | 
| `fuseBrandSeriesFilter`| Array             | No         | Array of mySQL table ID of fuse brand seires example S200 from ABB you want to include in return response      | 
| `fuseTypeFilter`       | Array             | No         | Array of mySQL table ID of fuse type you want to include in return response  |
| `fuseTypeSubFilter`    | Array             | No         | Array of mySQL table ID of fuse type sub filter you want to include in return response. |
| `fuseIDFilter`         | Array             | No         | Array of mySQL table ID of fuse ID you wan to include in return response. Normaly this is used when we want only to get information from a single cable. |
| `fuseSwitchLevelFilter`| Array             | No          | Array of mySQL table ID of switchLevel you want to include in return response. |

### Response
You will get a response `Object` with the following data:

| Field              | Type              | Description  |
|--------------------|-------------------|--------------|
| `fuse`             | Array Object      | Object array of fuse. | 
| `numRow`           | Number            | Number of cables returned |

### Example response
```
{
    "fuse": [
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
        },
        {
            "id": 4,
            "fuseBrandID": 2,
            "fuseTypeID": 1,
            "fuseTypeSubID": 2,
            "fuseSizeID": 10,
            "fuseBrandSeriesID": 3,
            "fuseSwitchLevelID": 1,
            "in": 13,
            "inAdjustable": 0,
            "fuseRCDSizeID": 2,
            "iRCDAdjustable": 0,
            "fuseName": "PKM2-13/2/B/003-A",
            "partnumber": null,
            "elnumber": 1654701,
            "numpoles": 2,
            "fuseBreakTypeID": 1,
            "fuseRCDTypeID": 1,
            "numPolesProtectected": 2,
            "fuseBrand": "Eaton",
            "fuseSize": 13,
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
        },
        {
            "id": 5,
            "fuseBrandID": 2,
            "fuseTypeID": 1,
            "fuseTypeSubID": 2,
            "fuseSizeID": 11,
            "fuseBrandSeriesID": 3,
            "fuseSwitchLevelID": 1,
            "in": 15,
            "inAdjustable": 0,
            "fuseRCDSizeID": 2,
            "iRCDAdjustable": 0,
            "fuseName": "PKM2-15/2/B/003-A-OL",
            "partnumber": null,
            "elnumber": 1654752,
            "numpoles": 2,
            "fuseBreakTypeID": 3,
            "fuseRCDTypeID": 1,
            "numPolesProtectected": 2,
            "fuseBrand": "Eaton",
            "fuseSize": 15,
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
            "name": "PKM2 - B-OL",
            "i1": 1.13,
            "i2": 1.3,
            "t2": 3600,
            "i4": 3,
            "i5": 4.8,
            "t5": 0.01,
            "iRCD": "30"
        },
        {
            "id": 6,
            "fuseBrandID": 2,
            "fuseTypeID": 1,
            "fuseTypeSubID": 2,
            "fuseSizeID": 12,
            "fuseBrandSeriesID": 3,
            "fuseSwitchLevelID": 1,
            "in": 16,
            "inAdjustable": 0,
            "fuseRCDSizeID": 2,
            "iRCDAdjustable": 0,
            "fuseName": "PKM2-16/2/B/003-A",
            "partnumber": null,
            "elnumber": 1654702,
            "numpoles": 2,
            "fuseBreakTypeID": 1,
            "fuseRCDTypeID": 1,
            "numPolesProtectected": 2,
            "fuseBrand": "Eaton",
            "fuseSize": 16,
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
        },
        {
            "id": 7,
            "fuseBrandID": 2,
            "fuseTypeID": 1,
            "fuseTypeSubID": 1,
            "fuseSizeID": 10,
            "fuseBrandSeriesID": 3,
            "fuseSwitchLevelID": 1,
            "in": 13,
            "inAdjustable": 0,
            "fuseRCDSizeID": 2,
            "iRCDAdjustable": 0,
            "fuseName": "PKM2-13/2/B/003-A",
            "partnumber": null,
            "elnumber": 1654701,
            "numpoles": 2,
            "fuseBreakTypeID": 1,
            "fuseRCDTypeID": 1,
            "numPolesProtectected": 2,
            "fuseBrand": "Eaton",
            "fuseSize": 13,
            "fuseBrandSeries": "PKPM2",
            "ue": [
                {
                    "max": 253,
                    "min": 196,
                    "type": "AC"
                }
            ],
            "fuseTypeSub": "MCB",
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
    ],
    "numRow": 5
}
```