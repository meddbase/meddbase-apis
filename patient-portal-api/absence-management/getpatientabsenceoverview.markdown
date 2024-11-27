---
layout: page
title: GetPatientAbsenceOverview
nav_order: 4
parent: Absence Management
---

# GetPatientAbsenceOverview

Returns a patient absence overview, which is limited to whether the patient is currently absent and the Bradford Factor score for the specified time period, or if no time period is specified, the previous 52 weeks. Does not show deleted absences.

## JavaScript library method

```javascript
patientportal.absences.getPatientAbsenceOverview({
    patient: <patient>,
    from: <date-from>,
    to: <date-to>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/absences/overview` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| patient | string | The patient key. |
| date-from | [DateTime](../objects-and-data-types/datetime) (optional) | The beginning date with which to calculate the patient’s Bradford Factor score (defaults to now minus 52 weeks). |
| date-to | [DateTime](../objects-and-data-types/datetime) (optional) | The end date with which to calculate the patient’s Bradford Factor score (defaults to now). |

## Returned JSON

```
{

"status": "ok",

"result": {

<[PatientAbsenceData](../objects-and-data-types/patientabsencedata\>

}

}
```
