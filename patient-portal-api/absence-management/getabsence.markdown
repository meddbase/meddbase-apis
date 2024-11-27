---
layout: page
title: GetAbsence
nav_order: 2
parent: Absence Management
---

# GetAbsence

Returns an absence record.

## JavaScript library method

```javascript
patientportal.absences.getAbsence({
    absence: <absence>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/absences/absence` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| absence | string | The key of the absence. |

## Returned JSON

```
{

"status": "ok",

"result": {

<[AbsenceData](../objects-and-data-types/absencedata)\>

}

}
```
