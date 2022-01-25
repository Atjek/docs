---
layout: default
title: List
nav_order: 2
parent : Cables
grand_parent : API
---

# List options
This will get you a list off all cables from a set of input parameters (if any set). 

### Request
You need to send a POST request with the following style example 
```
https://api.atjek.com/cables/list
```

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `cableIsolationFilter` | Array             | No         | Array of mySQL table ID of cableIsolation you want to include in return response |
| `cableTypeFilter`      | Array             | No         | Array of mySQL table ID of cableType you want to include in return response      | 
| `cableSizeFilter`      | Array             | No         | Array of mySQL table ID of cableSize you want to include in return response      | 
| `cableMaterialFilter`  | Array             | No         | Array of mySQL table ID of cableMaterial you want to include in return response  |
| `cableIDFilter`        | Array             | No         | Array of mySQL table ID of cable you want to include in return response. This is normaly used if you want information about one spesific cable |

### Response
You will get a response `Object` with the following data:

| Field              | Type              | Description  |
|--------------------|-------------------|--------------|
| `cables`           | Array Object      | Object array of cable. | 
| `numRow`           | Number            | Number of cables returned |
| `nekReturn`        |                   |                           |

### Example response
```
{
    "cables": [
        {
            "id": 9,
            "cableBrandID": 3,
            "cableTypeID": 2,
            "cableIsolationID": 1,
            "cableFireClassID": 0,
            "cores": 2,
            "nominelVoltage": 500,
            "frequency": 50,
            "maxUseTemperature": 70,
            "maxShortCircuitTemp": 150,
            "elnumber": 0,
            "cenelecNumber": "NO-N05VA5V-U",
            "modifyDate": "1",
            "useType": "1",
            "coreform": "1",
            "faseSizeID": 13,
            "faseMaterialID": 1,
            "nSizeID": null,
            "nMaterialID": null,
            "peSizeID": 13,
            "peMaterial": 1,
            "outerDim": 8,
            "screenDim": 7,
            "weight": 0.09,
            "centerDistanceCore": 3,
            "capacitance": 0.5,
            "resistance": 12.1,
            "inductance": 0,
            "capacitanceN": 0,
            "inductanceN": null,
            "resistancePE": 12.1,
            "inductancePE": 0,
            "rf_f": 24.1,
            "xf_f": 0.212,
            "rf_n": 0,
            "xf_n": 0,
            "rf_pe": 24.2,
            "xf_pe": 0.11596,
            "re": null,
            "edit": "2021-05-12T22:00:00.000Z",
            "deleted": 0,
            "name": "Standard",
            "cableName": "PR",
            "cableIsolation": "PVC",
            "material": "CU",
            "cableSize": 1.5,
            "peSize": 1.5,
            "faseMaterial": "CU"
        },
        {
            "id": 10,
            "cableBrandID": 3,
            "cableTypeID": 2,
            "cableIsolationID": 1,
            "cableFireClassID": 0,
            "cores": 2,
            "nominelVoltage": 500,
            "frequency": 50,
            "maxUseTemperature": 70,
            "maxShortCircuitTemp": 150,
            "elnumber": 0,
            "cenelecNumber": "NO-N05VA5V-U",
            "modifyDate": "1",
            "useType": "1",
            "coreform": "1",
            "faseSizeID": 14,
            "faseMaterialID": 1,
            "nSizeID": null,
            "nMaterialID": null,
            "peSizeID": 14,
            "peMaterial": 1,
            "outerDim": 9,
            "screenDim": 8,
            "weight": null,
            "centerDistanceCore": 4,
            "capacitance": 0.24,
            "resistance": 7.41,
            "inductance": 0.103,
            "capacitanceN": null,
            "inductanceN": null,
            "resistancePE": 7.41,
            "inductancePE": 0.103,
            "rf_f": 14.82,
            "xf_f": 0.206,
            "rf_n": 0,
            "xf_n": 0,
            "rf_pe": 14.82,
            "xf_pe": 0.10831,
            "re": null,
            "edit": "2021-05-12T22:00:00.000Z",
            "deleted": 0,
            "name": "Standard",
            "cableName": "PR",
            "cableIsolation": "PVC",
            "material": "CU",
            "cableSize": 2.5,
            "peSize": 2.5,
            "faseMaterial": "CU"
        },
    ],
    "numRow": 151,
    "nekReturn": [
        {
            "id": 9
        },
    ]
}
```

