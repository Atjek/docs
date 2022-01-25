---
layout: default
title: List
nav_order: 2
parent : Switchboard
grand_parent : API
---

# List options
This will get you a list off all switchboard you have access to.

### Request
You need to send a POST request with the following style example 
```
https://api.atjek.com/switchboard/list 
```

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `userID`               | Number            | Yes        | userID of the user you want switchbaord data on |


### Response
You will get a response `Object` with the following data:

| Field              | Type              | Description  |
|--------------------|-------------------|--------------|
| `switchBoard`      | Array Object      | Object array of switchboard for the user. | 

### Example response
```
{
    "switchBoard": [
        {
            "switchboardID": 11,
            "id": 11,
            "ref_id": "v3GSdwK2u5pE",
            "parent_id": null,
            "parentCircuitID": null,
            "name": "Motorfordeling",
            "identity": "+SA=433.100",
            "owner": null,
            "ik3pmax": "8",
            "ik3pmax_type": "2",
            "ik3pmax_cos": 0.8,
            "ik2pmin": "2",
            "ik2pmin_type": "2",
            "ik2pmin_cos": 0.8,
            "ijmax": "1000",
            "ijmax_type": "2",
            "ijmin": "2000",
            "ijmin_type": "2",
            "voltage": "230",
            "hertz": "50",
            "net_system": "1",
            "upward_circuit": null,
            "earth_resistance": null,
            "installerName": "Nordkontakt",
            "installerTelephone": "75556777",
            "installerEmail": "post@nordkontakt",
            "installerRegister": "123",
            "ownerMeterNumber": "123",
            "dateNew": null,
            "dateChanged": "2021-09-06T22:00:00.000Z",
            "ownerFirstName": "Bodø ",
            "ownerLastName": "Sildoljefabrikk",
            "ownerAdressStreetName": "Leitetunet",
            "ownerAdressStreetNumber": "2BA",
            "ownerAdressPostalCode": "8009",
            "ownerAdressPostalPlace": "Bodø",
            "ownerAdressSameAsParent": null,
            "countryID": 141,
            "normID": 1
        },
        {
            "switchboardID": 4,
            "id": 4,
            "ref_id": "2wJkvOYre7Va",
            "parent_id": 2,
            "parentCircuitID": null,
            "name": "Single board",
            "identity": "411.1.1",
            "owner": null,
            "ik3pmax": "10",
            "ik3pmax_type": "2",
            "ik3pmax_cos": 0.9,
            "ik2pmin": "2",
            "ik2pmin_type": "2",
            "ik2pmin_cos": 0.8,
            "ijmax": "1000",
            "ijmax_type": "2",
            "ijmin": "500",
            "ijmin_type": "2",
            "voltage": "230",
            "hertz": "50",
            "net_system": "3",
            "upward_circuit": null,
            "earth_resistance": null,
            "installerName": "Nordkontakt",
            "installerTelephone": null,
            "installerEmail": null,
            "installerRegister": null,
            "ownerMeterNumber": null,
            "dateNew": null,
            "dateChanged": "2021-05-13T22:00:00.000Z",
            "ownerFirstName": "Stian",
            "ownerLastName": "Rosenvinge2",
            "ownerAdressStreetName": "Leitetunet",
            "ownerAdressStreetNumber": "2B",
            "ownerAdressPostalCode": "8009",
            "ownerAdressPostalPlace": "Bodø",
            "ownerAdressSameAsParent": null,
            "countryID": 141,
            "normID": 1
        },
        {
            "switchboardID": 15,
            "id": 15,
            "ref_id": "j5D5JPaZBket",
            "parent_id": null,
            "parentCircuitID": null,
            "name": "Switchboard",
            "identity": "=433.001",
            "owner": null,
            "ik3pmax": "8",
            "ik3pmax_type": "2",
            "ik3pmax_cos": 0.8,
            "ik2pmin": "2",
            "ik2pmin_type": "2",
            "ik2pmin_cos": 0.8,
            "ijmax": "800",
            "ijmax_type": "2",
            "ijmin": "600",
            "ijmin_type": "2",
            "voltage": "230",
            "hertz": "50",
            "net_system": "1",
            "upward_circuit": null,
            "earth_resistance": "50",
            "installerName": "Nordkontakt",
            "installerTelephone": "755 05000",
            "installerEmail": "post@nordkontakt.no",
            "installerRegister": null,
            "ownerMeterNumber": null,
            "dateNew": null,
            "dateChanged": "2021-09-14T22:00:00.000Z",
            "ownerFirstName": "Stian",
            "ownerLastName": "Rosenvinge",
            "ownerAdressStreetName": "Leitetunet",
            "ownerAdressStreetNumber": "2B",
            "ownerAdressPostalCode": "8009",
            "ownerAdressPostalPlace": "Bodø",
            "ownerAdressSameAsParent": null,
            "countryID": 141,
            "normID": null
        }
    ]
}
``` 