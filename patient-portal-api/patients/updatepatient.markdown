---
layout: page
title: UpdatePatient
nav_order: 6
parent: Patients
---

# UpdatePatient

Updates the patient demographic data.

## JavaScript library method

```javascript
patientportal.patients.updatePatient({
    demog: <demog>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/patients/update-patient` |

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| demog | PersonDemographicData | Defines person’s details. |

## Returns

PersonDemographicData

## Remarks

Throws an exception if the patient doesn’t exist.
