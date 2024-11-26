---
layout: page
title: GetManagers
nav_order: 7
parent: Absence Management
---

# GetManagers

Gets the demographic data of the patient’s managers.

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
| patient | string | The patient key. |

## Returned JSON

```
{

"status": "ok",

"result": {

<list of [PatientDemographicData](#_PersonDemographicData)\>

}

}
```
