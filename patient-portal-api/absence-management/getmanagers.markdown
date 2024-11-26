---
layout: page
title: GetManagers
nav_order: 7
parent: Absence Management
---

# GetManagers

Gets the demographic data of the patient’s managers.

## JavaScript library method

```
patientportal.patients.getManagers ({

patient: &lt;patient&gt;

});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/patients/managers

## URL Parameters

| patient | string | The patient key. |
| --- | --- | --- |

## Returned JSON

```
{

"status": "ok",

"result": {

<list of [PatientDemographicData](#_PersonDemographicData)\>

}

}
```
