---
layout: page
title: GetPatient
nav_order: 5
parent: Patients
---

# GetPatient

Returns the specific patient.

## JavaScript library method

```javascript
patientportal.patients.getPatient({
    patient: <patient>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/patients/patient` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| patient | string | The key of the patient provided by the API upon GetPatients. |

## Returns

[PersonDemographicData](../objects-and-data-types/persondemographicdata)
