---
layout: page
title: GetAbsence
nav_order: 2
parent: Absence Management
---

# GetAbsence

Returns an absence record.

## JavaScript library method

```
patientportal.absences.getAbsence({

absence: &lt;absence&gt;

});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/absences/absence

## URL Parameters

| absence | string | The key of the absence. |
| --- | --- | --- |

## Returned JSON

```
{

"status": "ok",

"result": {

<[AbsenceData](#_AbsenceData)\>

}

}
```
