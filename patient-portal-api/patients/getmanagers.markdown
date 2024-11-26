---
layout: page
title: GetManagers
nav_order: 7
parent: Patients
---

# GetManagers

Returns the list of patient managers.

## JavaScript library method

```javascript
patientportal.patients.getManagers({
    patient: <patient>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/patients/managers` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| patient | string | The key of the patient provided by the API upon GetPatients. |

## Returns

PersonDemographicData\[\]
