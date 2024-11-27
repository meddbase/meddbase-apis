---
layout: page
title: SaveAbsence
nav_order: 3
parent: Absence Management
---

# SaveAbsence

Saves changes to an absence record. Any of the attributes in the [AbsenceData](../objects-and-data-types/absencedata) object can be modified and sent back to the API, but the only ones for which changes will be saved to the database are:

- EndDate
- LostWork.Days
- LostWork.Hours
- AccidentAtWork

## JavaScript library method

```javascript
patientportal.absences.saveAbsence({
    absenceData: <absence-data>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/absences/absence` |

## URL Parameters

| absence-data | [AbsenceData](../objects-and-data-types/absencedata) | The [AbsenceData](../objects-and-data-types/absencedata) object received from a call to the [GetAbsence](#_GetAbsence) method. |
| --- | --- | --- |

## Returned JSON

```
{

"status": "ok",

"result": {

<[AbsenceData](../objects-and-data-types/AbsenceData)\>

}

}
```
