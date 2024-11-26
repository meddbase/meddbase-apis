---
layout: page
title: ResendRTW
nav_order: 5
parent: Absence Management
---

# ResendRTW

Resends the questionnaire request email / SMS for the specified absence record to the patient. Sets the absence record’s questionnaire status to ‘sent’ if not already set.

## JavaScript library method

```javascript
patientportal.absences.resendRTW({
    absence: <absence>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/absences/resend-rtw` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| absence | string | The key of the absence. |

## Returned JSON

```
{

"status": "ok",

"result": {

<[AbsenceData](#_AbsenceData)\>

}

}
```
