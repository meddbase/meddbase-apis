---
layout: page
title: SetInsurer
nav_order: 9
parent: Patient
---

# SetInsurer

Sets a patient insurer. Only available for patient portal. Only public companies can be set.

## JavaScript library method

```javascript
patientportal.patient.setInsurer();
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/patient/insurer` |

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| insurerData | [InsurerData](../objects-and-data-types/insurerdata) | Patient’s insurer data to update. |

## POST data example

```
{

"insurerData": {

{

"Key": "1c5aabbdf813ad78c48cc8e6d8584162",

"MemberNumber": "Test member number"

}

}

}
```
