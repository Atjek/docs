---
layout: default
title: Switchboard
nav_order: 3
parent : Short circuit
grand_parent : API
---

# List Options
Will do a short circuit calculation of a switchboard with multiple incomming supplyes. Eg one og more generators.

### Request
You need to send a POST request with the following style example 
```
https://api.atjek.com/shortCircuit/switchBoard/ 
```

### parameters 

| Parameter              | Type              | Required ? | Description  |
|------------------------|-------------------|------------|--------------|
| `circuit`              | Array object      | Yes        | Array object of the circuit with equipment connected to the circuit in series. |

### Response
You will get a response `Object` with the following data:

| Field              | Type              | Description  |
|--------------------|-------------------|--------------|
| `shortcircuit`     | Object            | Object with all short circuit calculations for this switchboard.|

### Example input
```
{
   "circuit":[ 
      {
         "id":"",
         "circuitnumber":1,
         "circuitName":"Circuit",
         "numCores":2,
         "loadIn":10,
         "loadCos":0.8,
         "loadType":1,
         "loadStartTime":4.5,
         "loadStartIn":1,
         "loadDemandFactor":1,
         "loadEfficiency":1,
         "equipment":[
            {
               "id":320,
               "equipment_number":1,
               "equipmentName":"Generator",
               "equipmentID":3,
               "equipmentType":4,
               "terminalName":"X1",
               "terminalNumber":"",
               "cableRefInstMet":1,
               "cableLength":10,
               "cableCorFac":1,
               "cableTempCor":2,
               "cableOrientation":1,
               "cableDeltaFormation":1,
               "enabled":true,
               "type":"generator",
               "r":{
                  "value":0
               },
               "x0":0,
               "r0":0,
               "voltage":230,
               "sn":1000,
               "ikmaxToIkMin":1.24,
               "cFactor":0.95,
               "cFactorMax":1.05,
               "numDesimals":2,
               "xdPU":1.15,
               "xdTransPU":20,
               "xdSubPU":25,
               "zn":{
                  "value":0.0529,
                  "formula":"ZN = { 230^2 \\over 1000 \\cdot 10^3}",
                  "formula_raw":"ZN = { Un^2 \\over Sn}",
                  "unit":"&#8486;"
               },
               "xdSub":{
                  "value":1.3225,
                  "formula":"xd' = { 25 \\cdot 0.05 \\Omega }",
                  "formula_raw":"xd' = { xd'' \\cdot zn}",
                  "unit":"&#8486;"
               },
               "xdTrans":{
                  "value":1.058,
                  "formula":"xd'' = { 20 \\cdot 0.05 \\Omega }",
                  "formula_raw":"xd'' = { xd'' \\cdot zn}",
                  "unit":"&#8486;"
               },
               "xd":{
                  "value":0.060835,
                  "formula":"xd = { 1.15 \\cdot 0.05 \\Omega}",
                  "formula_raw":"xd = { xd \\cdot zn}",
                  "unit":"&#8486;"
               },
               "ik3pmaxSub":{
                  "value":0.17561551813075446,
                  "formula":"Ik'' = { 230 V \\over \\sqrt{3} \\cdot 1.32 \\Omega \\cdot 10^-3 }",
                  "formula_raw":"Ik'' = { Un \\over \\sqrt{3} \\cdot Xd'' }",
                  "unit":" kA"
               },
               "ik3pmaxTrans":{
                  "value":0.14049241450460354,
                  "formula":"Ik' = { 230 V \\over \\sqrt{3} \\cdot 1.06 \\Omega \\cdot 10^-3}",
                  "formula_raw":"Ik' = { Un \\over \\sqrt {3} \\cdot Xd' }",
                  "unit":" kA"
               },
               "ik3pmax":{
                  "value":0.008078313834014705,
                  "formula":" Ik = { 230 V \\over \\sqrt{3} \\cdot 0.06 \\Omega \\cdot 10^-3 }",
                  "formula_raw":"Ik = { Un \\over \\sqrt {3} \\cdot Xd }",
                  "unit":" kA"
               },
               "iShock":{
                  "value":0.43903879532688617,
                  "formula":"Is = {2.5 \\cdot 0.18 kA }",
                  "formula_raw":"Is = { 2,5 \\cdot Ik''}",
                  "unit":" kA"
               }
            }
         ],
         "showDetails":true
      },
      {
         "id":"",
         "circuitnumber":1,
         "circuitName":"Circuit",
         "numCores":2,
         "loadIn":10,
         "loadCos":0.8,
         "loadType":1,
         "loadStartTime":4.5,
         "loadStartIn":1,
         "loadDemandFactor":1,
         "loadEfficiency":1,
         "equipment":[
            {
               "id":320,
               "equipment_number":1,
               "equipmentName":"Generator",
               "equipmentID":3,
               "equipmentType":4,
               "terminalName":"X1",
               "terminalNumber":"",
               "cableRefInstMet":1,
               "cableLength":10,
               "cableCorFac":1,
               "cableTempCor":2,
               "cableOrientation":1,
               "cableDeltaFormation":1,
               "enabled":true,
               "type":"generator",
               "r":{
                  "value":0
               },
               "x0":0,
               "r0":0,
               "voltage":230,
               "sn":1000,
               "ikmaxToIkMin":1.24,
               "cFactor":0.95,
               "cFactorMax":1.05,
               "numDesimals":2,
               "xdPU":1.15,
               "xdTransPU":20,
               "xdSubPU":25,
               "zn":{
                  "value":0.0529,
                  "formula":"ZN = { 230^2 \\over 1000 \\cdot 10^3}",
                  "formula_raw":"ZN = { Un^2 \\over Sn}",
                  "unit":"&#8486;"
               },
               "xdSub":{
                  "value":1.3225,
                  "formula":"xd' = { 25 \\cdot 0.05 \\Omega }",
                  "formula_raw":"xd' = { xd'' \\cdot zn}",
                  "unit":"&#8486;"
               },
               "xdTrans":{
                  "value":1.058,
                  "formula":"xd'' = { 20 \\cdot 0.05 \\Omega }",
                  "formula_raw":"xd'' = { xd'' \\cdot zn}",
                  "unit":"&#8486;"
               },
               "xd":{
                  "value":0.060835,
                  "formula":"xd = { 1.15 \\cdot 0.05 \\Omega}",
                  "formula_raw":"xd = { xd \\cdot zn}",
                  "unit":"&#8486;"
               },
               "ik3pmaxSub":{
                  "value":0.17561551813075446,
                  "formula":"Ik'' = { 230 V \\over \\sqrt{3} \\cdot 1.32 \\Omega \\cdot 10^-3 }",
                  "formula_raw":"Ik'' = { Un \\over \\sqrt{3} \\cdot Xd'' }",
                  "unit":" kA"
               },
               "ik3pmaxTrans":{
                  "value":0.14049241450460354,
                  "formula":"Ik' = { 230 V \\over \\sqrt{3} \\cdot 1.06 \\Omega \\cdot 10^-3}",
                  "formula_raw":"Ik' = { Un \\over \\sqrt {3} \\cdot Xd' }",
                  "unit":" kA"
               },
               "ik3pmax":{
                  "value":0.008078313834014705,
                  "formula":" Ik = { 230 V \\over \\sqrt{3} \\cdot 0.06 \\Omega \\cdot 10^-3 }",
                  "formula_raw":"Ik = { Un \\over \\sqrt {3} \\cdot Xd }",
                  "unit":" kA"
               },
               "iShock":{
                  "value":0.43903879532688617,
                  "formula":"Is = {2.5 \\cdot 0.18 kA }",
                  "formula_raw":"Is = { 2,5 \\cdot Ik''}",
                  "unit":" kA"
               }
            }
         ],
         "showDetails":true
      }
   ]
}
```

### Example response
```
"shortcircuit"{
   "riMax":0,
   "xiMax":0.060835,
   "xiMaxSub":1.3225,
   "xiMaxTrans":1.058,
   "x0Max":0,
   "r0Max":0,
   "ziMax":0.060835,
   "riMin":0,
   "xiMin":0.060835,
   "r0Min":0,
   "x0Min":0.060835,
   "voltage":230,
   "ikmaxToIkMin":1.24,
   "cFactor":0.95,
   "cFactorMax":1.05,
   "numDesimals":2,
   "R0Max":9,
   "X0max":7,
   "ziMin":2,
   "zPE":1,
   "rpeCable":1,
   "xpeCable":1,
   "ik3pmax":{
      "value":2291.93868676411,
      "formula":"Ik3pMax = { 1.05 \\cdot 230V \\over  \\sqrt{ 3 \\cdot0.06} \\Omega}",
      "formula_raw":"Ik3pmax ={ C \\cdot Un \\over \\sqrt 3 \\cdot Zikmax}",
      "unit":"kA"
   },
   "ik2pMax":{
      "value":1984.8771266540643,
      "formula":"Ik2pMax = { 1.05\\cdot 230V \\over 2 \\cdot 0.06 \\Omega}",
      "formula_raw":"Ik2pmaks ={ c \\cdot Un \\over 2 \\cdot Zikmaks}",
      "unit":"kA"
   },
   "ik1pMax":{
      "value":36.44642170551313,
      "formula":"Ik1pMax = \\sqrt{3} \\cdot 0.95 \\cdot 230V \\over \\sqrt {(2 \\cdot 0.00 \\Omega + 9.00 \\Omega )^2 + {2 \\cdot 0.06 \\Omega + 7.00 \\Omega^2}} ",
      "formula_raw":"Ik1pMax = { \\sqrt{3} \\cdot c \\cdot Un \\over \\sqrt {(2 \\cdot Rikmax + R0ikmax)^2 + (2 \\cdot Xikmax + X0ikmax)^2}}",
      "unit":"kA"
   },
   "ik2pMin":{
      "value":54.625,
      "formula":"Ik2pMin = { 0.95 \\cdot 230V \\over (2 \\cdot 2.00  \\Omega) }",
      "formula_raw":"Ik2pMin = {C \\cdot U \\over \\ 2 \\cdot ziMin}",
      "unit":"kA"
   },
   "ik1pMin":{
      "value":2073.6588118341942,
      "formula":"Ik1pMin = {\\sqrt{3} \\cdot 0.95 \\cdot 230V \\over (2 \\cdot 0.00 \\Omega+ 0.00 \\Omega)^2 + (2 \\cdot 0.06 \\Omega+ 0.06\\Omega)^2 }",
      "formula_raw":"Ik1pMin = {\\sqrt{3} \\cdot c \\cdot Un \\over (2 \\cdot 2Rmin + R0Min)^2 + (2 \\cdot 2Xmin + X0min)^2}",
      "unit":"kA"
   },
   "VoltageUC":{
      "value":2073.6588118341942,
      "formula":"Uc = { 2073.66kA \\cdot 1.00 \\Omega}",
      "formula_raw":"Uc = {Ik1pmin \\cdot Zpe}",
      "unit":"V"
   },
   "ij1pMin":{
      "value":74.93834212834965,
      "formula":"Ij1pMin = {0.95 \\cdot 230V \\over 2 \\cdot \\sqrt{ 0.00 \\Omega + 1.00 \\Omega ^2 0.06\\Omega + 1.00\\Omega ^2 }}",
      "formula_raw":"Ij1pMin = { C \\cdot U \\over 2 \\cdot \\sqrt{(riMin \\Omega + RPEcable \\Omega) ^2 + (xiMin \\Omega + xpeCable \\Omega)^2}}",
      "unit":"kA"
   }
}
```