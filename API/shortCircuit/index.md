---
layout: default
title: Short circuit
nav_order: 6
parent : API
has_children: true
---

# Equipment
 

router.post('/switchBoard',             shortCircuitNet.switchBoard); 
router.post('/net/multiple',            shortCircuitNet.calculateCircuit); 
router.post('/net/impedance',           shortCircuitNet.impedance);
router.post("/transformer/calculate",   transformer.calculate);
router.post('/generator/calculate',     generator.generatorCalc);