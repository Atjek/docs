---
layout: default
title: View
nav_order: 3
parent : Switchboard
grand_parent : API
---

# List options
This will view a switchboard, and get you a list of all circuits connected to the switchboard. Inside the circuits object you will get a nested list of all equipment, and short circuit calculations for each circuit.  

### Request
You need to send a POST request with the following style example 
```
https://api.atjek.com/switchboard/view/SWITCHBOARDID 
```

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `SWITCHBOARDID`        | String            | Yes        | Unique switchboard ID for that switchboard. |

After you have opened a switchboard for the first time, the switchboard get`s added to the list of switchboard you have access to. 

### Response
You will get a response `Object` with the following data:

| Field              | Type              | Description  |
|--------------------|-------------------|--------------|
| `switchBoard`      | Array Object      | Object array of switchboard with data. |
| `circuits`         | Array Object      | Object array of circuits connected to that switchboard. Eqipment to one spesific circuit is a nested Array of the cirucit inside `equipment`. Also contains a nested `shortCircuitCalculation` with short circuit calculations for that circuit. |
| `supplyCircuit`    | Array Object      | Object array of supply circuit. Same data and structure as any other circuit. |
| `cables`           | Array Object      | Object array of all cables used in all the circuits for this switchboard.     |
| `fuse`             | Array Object      | Object array of all fuses used in all the circuits for this switchboard.  |
| `normOptions`      | Array Object      | Object array of all norms available for this country for this switchboard. Normaly all newer than the norm for the switchboard. |
| `usedNorms`        | Array Object      | Object array of all norms used in all the circuits for this switchboard. | 

### Example response
```
{
    "switchboard": [
        {
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
            "normID": null,
            "countryName": "Norway"
        }
    ],
    "circuits": [
        {
            "id": 186,
            "circuitnumber": "2",
            "circuitName": "Induksjonstopp",
            "loadType": "1",
            "loadIn": "10",
            "loadCos": 0.8,
            "loadStartTime": 4.5,
            "loadStartIn": 1,
            "loadDemandFactor": 1,
            "loadEfficiency": 1,
            "switchboardID": 15,
            "deleted": 0,
            "numCores": 2,
            "connectedFase": 0,
            "normID": 1,
            "equipment": [
                {
                    "id": 280,
                    "equipment_number": "1",
                    "equipmentID": "6",
                    "equipmentName": "XF",
                    "deleted": 0,
                    "switchboardCircuitID": 186,
                    "equipmentType": 1,
                    "terminalName": "X1",
                    "terminalNumber": "",
                    "cableRefInstMet": "1",
                    "cableLength": "10",
                    "cableCorFac": "1",
                    "cableTempCor": "2",
                    "cableOrientation": 1,
                    "cableDeltaFormation": 1
                },
                {
                    "id": 281,
                    "equipment_number": "2",
                    "equipmentID": "23",
                    "equipmentName": "W001",
                    "deleted": 0,
                    "switchboardCircuitID": 186,
                    "equipmentType": 2,
                    "terminalName": "X1",
                    "terminalNumber": "",
                    "cableRefInstMet": "1",
                    "cableLength": "15",
                    "cableCorFac": "1",
                    "cableTempCor": "2",
                    "cableOrientation": 1,
                    "cableDeltaFormation": 1
                }
            ],
            "shortCircuitCalculation": {
                "constants": {
                    "ikmaxToIkMin": 1.24
                },
                "numDesimals": 2,
                "inputLoadAmp": "10",
                "inputLoadCosPhi": 0.8,
                "inputLoadThreePhase": 2,
                "cableLength": "15",
                "cableROhm": 4.61,
                "cableXOhm": 0.095085,
                "voltage": 200,
                "Ik3pmaxInput": "8",
                "cosPhiMaxInput": 0.8,
                "ik2pminInput": "2",
                "cosPhiMinInput": 0.8,
                "rpeCable": 4.61,
                "xpeCable": 0.095085,
                "zOhmNetMax": {
                    "value": 16.598820239201743,
                    "formula": "ZNetMax = { 230V \\over \\sqrt {3} \\cdot8kA }",
                    "formula_raw": "ZnetMax = { Un \\over \\sqrt{3} \\cdot Ik3pmax }",
                    "unit": "&#8486;"
                },
                "rOhmNetMax": {
                    "value": 13.279056191361395,
                    "formula": "RNetMax = { 16.60\\Omega \\cdot 0.80}",
                    "formula_raw": "RNetMax = {Znett \\cdot cos\\phi max}",
                    "unit": "&#8486;"
                },
                "xOhmNetMax": {
                    "value": 9.959292143521045,
                    "formula": "XNetMax = { \\sqrt { 16.60\\Omega ^2 - 13.28\\Omega ^2}}",
                    "formula_raw": "XNetMax = {\\sqrt {Znett^2 - Rimax^2}}",
                    "unit": "&#8486;"
                },
                "zOhmNetMin": {
                    "value": 54.625,
                    "formula": "ZNetMin = { 0.95 \\cdot 230V \\over 2 \\cdot 2 kA}",
                    "formula_raw": "ZnetMin = {C \\cdot U \\over 2 \\cdot Ik2pMin}",
                    "unit": "&#8486;"
                },
                "rOhmNetMin": {
                    "value": 43.7,
                    "formula": "RikMin = {54.63\\Omega \\cdot 0.8}",
                    "formula_raw": "RNetMin = {ZNetMin \\cdot \\phi Min}",
                    "unit": "&#8486;"
                },
                "xOhmNetMin": {
                    "value": 32.775,
                    "formula": "XikMin = {\\sqrt {54.63\\Omega^2 - 43.70\\Omega^2}}",
                    "formula_raw": "XNetMin = {\\sqrt{ZNetMin^2 - XNetMin^2}}",
                    "unit": "&#8486;"
                },
                "rCable": {
                    "value": 69.15,
                    "formula": "RCable = {4.61 \\Omega \\cdot 15m }",
                    "formula_raw": "Rcable = {Rcable \\cdot l}",
                    "unit": "&#8486;"
                },
                "xCable": {
                    "value": 1.426275,
                    "formula": "XCable = {0.095085 \\Omega \\cdot 15m }",
                    "formula_raw": "Xcable = {XCable \\cdot l}",
                    "unit": "&#8486;"
                },
                "r0max": {
                    "value": 276.6,
                    "formula": "R0ikmax = {69.15\\Omega + 3 \\cdot 69.15m}",
                    "formula_raw": "R0ikmax = {Rcable \\cdot l}",
                    "unit": "&#8486;"
                },
                "x0max": {
                    "value": 4.278824999999999,
                    "formula": "X0ikmax = { 3 \\cdot1.426275\\Omega}",
                    "formula_raw": "X0ikmax = {3 \\cdot Xcable}",
                    "unit": "&#8486;"
                },
                "rCableMin": {
                    "value": 85.74600000000001,
                    "formula": "RCableMin = { 4.61 \\Omega \\cdot 15 m\\cdot 1.24}",
                    "formula_raw": "RCableMin = {Rcable \\cdot l \\cdot kt2}"
                },
                "xCableMin": {
                    "value": 1.426275,
                    "formula": "RCableMin = { 0.095085 \\Omega \\cdot 15 m}",
                    "formula_raw": "RCableMin = {Rcable \\cdot l}"
                },
                "r0min": {
                    "value": 342.98400000000004,
                    "formula": "R0ikmax = {85.74600000000001\\Omega + 3 \\cdot 85.74600000000001}",
                    "formula_raw": "R0ikmax = {Rcable \\cdot l}",
                    "unit": "&#8486;"
                },
                "x0min": {
                    "value": 4.278824999999999,
                    "formula": "X0ikmax = { 3 \\cdot1.426275\\Omega}",
                    "formula_raw": "X0ikmax = {3 \\cdot Xcable}",
                    "unit": "&#8486;"
                },
                "zpeCableMin": {
                    "value": 85.75786130947779,
                    "formula": "",
                    "unit": "&#8486;"
                },
                "xiMax": {
                    "value": 11.385567143521046,
                    "unit": "&#8486;"
                },
                "riMax": {
                    "value": 82.4290561913614,
                    "unit": "&#8486;"
                },
                "ziMax": {
                    "value": 83.21166050367124,
                    "formula": "Z = { \\sqrt{ 82.43^2 \\cdot11.39^2 }}",
                    "unit": "&#8486;"
                },
                "riMin": {
                    "value": 129.44600000000003,
                    "unit": "&#8486;"
                },
                "xiMin": {
                    "value": 34.201274999999995,
                    "unit": "&#8486;"
                },
                "ziMin": {
                    "value": 133.8879909761351,
                    "formula": "Z = { \\sqrt{ 129.45^2 \\cdot34.20^2 }}",
                    "unit": "&#8486;"
                },
                "r0Min": 43.7,
                "x0Min": 32.775,
                "ik3pmax": {
                    "value": 1.6756075911157076,
                    "formula": "Ik3pMax = { 1.05 \\cdot 230V \\over  \\sqrt{ 3 \\cdot83.21} \\Omega}",
                    "formula_raw": "Ik3pmax ={ C \\cdot Un \\over \\sqrt 3 \\cdot Zikmax}",
                    "unit": "kA"
                },
                "ik2pMax": {
                    "value": 1.451118740680251,
                    "formula": "Ik2pMax = { 1.05\\cdot 230V \\over 2 \\cdot 83.21 \\Omega}",
                    "formula_raw": "Ik2pmaks ={ c \\cdot Un \\over 2 \\cdot Zikmaks}",
                    "unit": "kA"
                },
                "ik2pMin": {
                    "value": 0.8159805760284603,
                    "formula": "Ik2pMin = { 0.95 \\cdot 230V \\over (2 \\cdot 133.89  \\Omega) }",
                    "formula_raw": "Ik2pMin = {C \\cdot U \\over \\ 2 \\cdot ziMin}",
                    "unit": "kA"
                },
                "VoltageUC": {
                    "value": 120.10182216253116,
                    "formula": "Uc = { 1.40kA \\cdot 85.76 \\Omega}",
                    "formula_raw": "Uc = {Ik1pmin \\cdot Zpe}",
                    "unit": "V"
                },
                "ij1pMin": {
                    "value": 0.7895292522589493,
                    "formula": "Ij1pMin = {0.95 \\cdot 230V \\over 2 \\cdot \\sqrt{ 129.45 \\Omega + 4.61 \\Omega ^2 34.20\\Omega + 0.10\\Omega ^2 }}",
                    "formula_raw": "Ij1pMin = { C \\cdot U \\over 2 \\cdot \\sqrt{(riMin \\Omega + RPEcable \\Omega) ^2 + (xiMin \\Omega + xpeCable \\Omega)^2}}",
                    "unit": "kA"
                },
                "voltageDrop": {
                    "value": 1.371936,
                    "formula": "\\Delta U = {10A \\cdot 4.61 \\Omega \\cdot 10^-3 \\cdot 1.24 \\cdot 15m \\cdot 0.8 \\cdot 2}",
                    "formula_raw": "\\Delta U = { Aload \\cdot rCable \\Omega \\cdot 10^3 \\cdot 1.24 \\cdot m \\cdot \\phi \\cdot 2 }",
                    "unit": "V"
                },
                "voltageDropPercent": {
                    "value": 0.5964939130434783,
                    "formula": " \\Delta U = {1.37V \\cdot 100 \\over 230V}",
                    "formula_raw": "\\Delta U = {\\Delta U \\cdot 100 \\over Un}",
                    "unit": "%"
                },
                "ikmaxToIkMin": 1.24,
                "cFactor": 0.95,
                "cFactorMax": 1.05,
                "rpeCableMin": {
                    "value": 85.74600000000001,
                    "formula": "RpeMin = { 4.61\\Omega \\cdot 1.24 \\cdot 15m}",
                    "unit": "&#8486;"
                },
                "xpeCableMin": {
                    "value": 1.426275,
                    "formula": "xpeMin = {0.095085\\Omega \\cdot 15m}",
                    "unit": "&#8486;"
                }
            }
        },
        {
            "id": 187,
            "circuitnumber": "4",
            "circuitName": "Komfyrtopp",
            "loadType": "1",
            "loadIn": "16",
            "loadCos": 0.8,
            "loadStartTime": 4.5,
            "loadStartIn": 1,
            "loadDemandFactor": 1,
            "loadEfficiency": 1,
            "switchboardID": 15,
            "deleted": 0,
            "numCores": 2,
            "connectedFase": 0,
            "normID": 1,
            "equipment": [
                {
                    "id": 283,
                    "equipment_number": "1",
                    "equipmentID": "6",
                    "equipmentName": "XF",
                    "deleted": 0,
                    "switchboardCircuitID": 187,
                    "equipmentType": 1,
                    "terminalName": "X1",
                    "terminalNumber": "",
                    "cableRefInstMet": "1",
                    "cableLength": "10",
                    "cableCorFac": "1",
                    "cableTempCor": "2",
                    "cableOrientation": 1,
                    "cableDeltaFormation": 1
                },
                {
                    "id": 284,
                    "equipment_number": "2",
                    "equipmentID": "9",
                    "equipmentName": "W",
                    "deleted": 0,
                    "switchboardCircuitID": 187,
                    "equipmentType": 2,
                    "terminalName": "X1",
                    "terminalNumber": "",
                    "cableRefInstMet": "5",
                    "cableLength": " 20",
                    "cableCorFac": "1",
                    "cableTempCor": "5",
                    "cableOrientation": 1,
                    "cableDeltaFormation": 1
                },
                {
                    "id": 290,
                    "equipment_number": "4",
                    "equipmentID": "9",
                    "equipmentName": "W",
                    "deleted": 0,
                    "switchboardCircuitID": 187,
                    "equipmentType": 2,
                    "terminalName": "X1",
                    "terminalNumber": "",
                    "cableRefInstMet": "3",
                    "cableLength": "10",
                    "cableCorFac": "1",
                    "cableTempCor": "2",
                    "cableOrientation": 1,
                    "cableDeltaFormation": 1
                }
            ],
            "shortCircuitCalculation": {
                "constants": {
                    "ikmaxToIkMin": 1.24
                },
                "numDesimals": 2,
                "inputLoadAmp": "16",
                "inputLoadCosPhi": 0.8,
                "inputLoadThreePhase": 2,
                "cableLength": "10",
                "cableROhm": 24.2,
                "cableXOhm": 0,
                "voltage": 200,
                "Ik3pmaxInput": "8",
                "cosPhiMaxInput": 0.8,
                "ik2pminInput": "2",
                "cosPhiMinInput": 0.8,
                "rpeCable": 24.2,
                "xpeCable": 0,
                "zOhmNetMax": {
                    "value": 16.598820239201743,
                    "formula": "ZNetMax = { 230V \\over \\sqrt {3} \\cdot8kA }",
                    "formula_raw": "ZnetMax = { Un \\over \\sqrt{3} \\cdot Ik3pmax }",
                    "unit": "&#8486;"
                },
                "rOhmNetMax": {
                    "value": 13.279056191361395,
                    "formula": "RNetMax = { 16.60\\Omega \\cdot 0.80}",
                    "formula_raw": "RNetMax = {Znett \\cdot cos\\phi max}",
                    "unit": "&#8486;"
                },
                "xOhmNetMax": {
                    "value": 9.959292143521045,
                    "formula": "XNetMax = { \\sqrt { 16.60\\Omega ^2 - 13.28\\Omega ^2}}",
                    "formula_raw": "XNetMax = {\\sqrt {Znett^2 - Rimax^2}}",
                    "unit": "&#8486;"
                },
                "zOhmNetMin": {
                    "value": 54.625,
                    "formula": "ZNetMin = { 0.95 \\cdot 230V \\over 2 \\cdot 2 kA}",
                    "formula_raw": "ZnetMin = {C \\cdot U \\over 2 \\cdot Ik2pMin}",
                    "unit": "&#8486;"
                },
                "rOhmNetMin": {
                    "value": 43.7,
                    "formula": "RikMin = {54.63\\Omega \\cdot 0.8}",
                    "formula_raw": "RNetMin = {ZNetMin \\cdot \\phi Min}",
                    "unit": "&#8486;"
                },
                "xOhmNetMin": {
                    "value": 32.775,
                    "formula": "XikMin = {\\sqrt {54.63\\Omega^2 - 43.70\\Omega^2}}",
                    "formula_raw": "XNetMin = {\\sqrt{ZNetMin^2 - XNetMin^2}}",
                    "unit": "&#8486;"
                },
                "rCable": {
                    "value": 242,
                    "formula": "RCable = {24.2 \\Omega \\cdot 10m }",
                    "formula_raw": "Rcable = {Rcable \\cdot l}",
                    "unit": "&#8486;"
                },
                "xCable": {
                    "value": 0,
                    "formula": "XCable = {0 \\Omega \\cdot 10m }",
                    "formula_raw": "Xcable = {XCable \\cdot l}",
                    "unit": "&#8486;"
                },
                "r0max": {
                    "value": 968,
                    "formula": "R0ikmax = {242\\Omega + 3 \\cdot 242m}",
                    "formula_raw": "R0ikmax = {Rcable \\cdot l}",
                    "unit": "&#8486;"
                },
                "x0max": {
                    "value": 0,
                    "formula": "X0ikmax = { 3 \\cdot0\\Omega}",
                    "formula_raw": "X0ikmax = {3 \\cdot Xcable}",
                    "unit": "&#8486;"
                },
                "rCableMin": {
                    "value": 300.08,
                    "formula": "RCableMin = { 24.2 \\Omega \\cdot 10 m\\cdot 1.24}",
                    "formula_raw": "RCableMin = {Rcable \\cdot l \\cdot kt2}"
                },
                "xCableMin": {
                    "value": 0,
                    "formula": "RCableMin = { 0 \\Omega \\cdot 10 m}",
                    "formula_raw": "RCableMin = {Rcable \\cdot l}"
                },
                "r0min": {
                    "value": 1200.32,
                    "formula": "R0ikmax = {300.08\\Omega + 3 \\cdot 300.08}",
                    "formula_raw": "R0ikmax = {Rcable \\cdot l}",
                    "unit": "&#8486;"
                },
                "x0min": {
                    "value": 0,
                    "formula": "X0ikmax = { 3 \\cdot0\\Omega}",
                    "formula_raw": "X0ikmax = {3 \\cdot Xcable}",
                    "unit": "&#8486;"
                },
                "zpeCableMin": {
                    "value": 300.08,
                    "formula": "",
                    "unit": "&#8486;"
                },
                "xiMax": {
                    "value": 9.959292143521045,
                    "unit": "&#8486;"
                },
                "riMax": {
                    "value": 255.2790561913614,
                    "unit": "&#8486;"
                },
                "ziMax": {
                    "value": 255.47325501890066,
                    "formula": "Z = { \\sqrt{ 255.28^2 \\cdot9.96^2 }}",
                    "unit": "&#8486;"
                },
                "riMin": {
                    "value": 343.78,
                    "unit": "&#8486;"
                },
                "xiMin": {
                    "value": 32.775,
                    "unit": "&#8486;"
                },
                "ziMin": {
                    "value": 345.33880324255483,
                    "formula": "Z = { \\sqrt{ 343.78^2 \\cdot32.77^2 }}",
                    "unit": "&#8486;"
                },
                "r0Min": 43.7,
                "x0Min": 32.775,
                "ik3pmax": {
                    "value": 0.5457717677687208,
                    "formula": "Ik3pMax = { 1.05 \\cdot 230V \\over  \\sqrt{ 3 \\cdot255.47} \\Omega}",
                    "formula_raw": "Ik3pmax ={ C \\cdot Un \\over \\sqrt 3 \\cdot Zikmax}",
                    "unit": "kA"
                },
                "ik2pMax": {
                    "value": 0.47265221555605325,
                    "formula": "Ik2pMax = { 1.05\\cdot 230V \\over 2 \\cdot 255.47 \\Omega}",
                    "formula_raw": "Ik2pmaks ={ c \\cdot Un \\over 2 \\cdot Zikmaks}",
                    "unit": "kA"
                },
                "ik2pMin": {
                    "value": 0.316355992938524,
                    "formula": "Ik2pMin = { 0.95 \\cdot 230V \\over (2 \\cdot 345.34  \\Omega) }",
                    "formula_raw": "Ik2pMin = {C \\cdot U \\over \\ 2 \\cdot ziMin}",
                    "unit": "kA"
                },
                "VoltageUC": {
                    "value": 163.9097971392321,
                    "formula": "Uc = { 0.55kA \\cdot 300.08 \\Omega}",
                    "formula_raw": "Uc = {Ik1pmin \\cdot Zpe}",
                    "unit": "V"
                },
                "ij1pMin": {
                    "value": 0.29572047853240285,
                    "formula": "Ij1pMin = {0.95 \\cdot 230V \\over 2 \\cdot \\sqrt{ 343.78 \\Omega + 24.20 \\Omega ^2 32.77\\Omega + 0.00\\Omega ^2 }}",
                    "formula_raw": "Ij1pMin = { C \\cdot U \\over 2 \\cdot \\sqrt{(riMin \\Omega + RPEcable \\Omega) ^2 + (xiMin \\Omega + xpeCable \\Omega)^2}}",
                    "unit": "kA"
                },
                "voltageDrop": {
                    "value": 7.682048000000001,
                    "formula": "\\Delta U = {16A \\cdot 24.2 \\Omega \\cdot 10^-3 \\cdot 1.24 \\cdot 10m \\cdot 0.8 \\cdot 2}",
                    "formula_raw": "\\Delta U = { Aload \\cdot rCable \\Omega \\cdot 10^3 \\cdot 1.24 \\cdot m \\cdot \\phi \\cdot 2 }",
                    "unit": "V"
                },
                "voltageDropPercent": {
                    "value": 3.3400208695652176,
                    "formula": " \\Delta U = {7.68V \\cdot 100 \\over 230V}",
                    "formula_raw": "\\Delta U = {\\Delta U \\cdot 100 \\over Un}",
                    "unit": "%"
                },
                "ikmaxToIkMin": 1.24,
                "cFactor": 0.95,
                "cFactorMax": 1.05,
                "rpeCableMin": {
                    "value": 300.08,
                    "formula": "RpeMin = { 24.2\\Omega \\cdot 1.24 \\cdot 10m}",
                    "unit": "&#8486;"
                },
                "xpeCableMin": {
                    "value": 0,
                    "formula": "xpeMin = {0\\Omega \\cdot 10m}",
                    "unit": "&#8486;"
                }
            }
        }
    ],
    "supplyCircuit": {
        "id": 0,
        "circuitnumber": "23",
        "circuitName": "testnacm",
        "loadType": "1",
        "loadIn": "10",
        "loadCos": 0.8,
        "loadStartTime": 1,
        "loadStartIn": 1,
        "loadDemandFactor": 0.4,
        "loadEfficiency": 1,
        "switchboardID": 4,
        "deleted": 0,
        "numCores": 1,
        "normID": 1,
        "equipment": [
            {
                "id": 240,
                "equipment_number": "2",
                "equipmentID": 3,
                "equipmentName": "XF",
                "deleted": 0,
                "switchboardCircuitID": 11,
                "equipmentType": 1,
                "terminalName": "X1",
                "terminalNumber": "",
                "cableRefInstMet": "3",
                "cableLength": "10",
                "cableCorFac": "1",
                "cableTempCor": "5",
                "cableOrientation": null,
                "cableDeltaFormation": null
            },
            {
                "id": 124,
                "equipment_number": "1",
                "equipmentID": 7,
                "equipmentName": "W12",
                "deleted": 0,
                "switchboardCircuitID": 11,
                "equipmentType": 2,
                "terminalName": "X1",
                "terminalNumber": "123",
                "cableRefInstMet": "5",
                "cableLength": "12",
                "cableCorFac": null,
                "cableTempCor": null,
                "cableOrientation": null,
                "cableDeltaFormation": null
            }
        ]
    },
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
            "id": 23,
            "cableBrandID": 3,
            "cableTypeID": 3,
            "cableIsolationID": 1,
            "cableFireClassID": 0,
            "cores": 2,
            "nominelVoltage": 750,
            "frequency": 50,
            "maxUseTemperature": 70,
            "maxShortCircuitTemp": 150,
            "elnumber": 0,
            "cenelecNumber": "HO7V-U",
            "modifyDate": "1",
            "useType": "1",
            "coreform": "1",
            "faseSizeID": 15,
            "faseMaterialID": 1,
            "nSizeID": null,
            "nMaterialID": null,
            "peSizeID": 15,
            "peMaterial": 1,
            "outerDim": 4,
            "screenDim": 0,
            "weight": 0.141,
            "centerDistanceCore": 4,
            "capacitance": 0.27,
            "resistance": 4.61,
            "inductance": 0.095085,
            "capacitanceN": null,
            "inductanceN": null,
            "resistancePE": 4.61,
            "inductancePE": 0.095085,
            "rf_f": 9.22,
            "xf_f": 0.19017,
            "rf_n": null,
            "xf_n": null,
            "rf_pe": 9.22,
            "xf_pe": 0.23372,
            "re": null,
            "edit": "2021-05-12T22:00:00.000Z",
            "deleted": 0,
            "name": "Standard",
            "cableName": "PN",
            "cableIsolation": "PVC",
            "material": "CU",
            "cableSize": 4,
            "peSize": 4,
            "faseMaterial": "CU"
        }
    ],
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
        }
    ],
    "normOptions": [
        {
            "id": 1,
            "countryID": 141,
            "normName": "NEK400:2018 NO",
            "fileName": "NEK400_2018_NO",
            "version": 10
        },
        {
            "id": 2,
            "countryID": 141,
            "normName": "NEK400:2014 NO",
            "fileName": "NEK400_2014_NO",
            "version": 9
        },
        {
            "id": 3,
            "countryID": 141,
            "normName": "NEK400_2010",
            "fileName": "NEK400_2010_NO",
            "version": 8
        },
        {
            "id": 4,
            "countryID": 141,
            "normName": "NEK400_2006",
            "fileName": "NEK400_2006_NO",
            "version": 7
        }
    ],
    "usedNorms": [
        {
            "id": 1,
            "countryID": 141,
            "normName": "NEK400:2018 NO",
            "fileName": "NEK400_2018_NO",
            "version": 10
        }
    ]
}
```