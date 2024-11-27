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

## Returns

[AbsenceData](../objects-and-data-types/absencedata)

## Returned JSON

```json
{
    "status": "ok",
    "result": {
        "Patient": {
            "Title": "Mr",
            "Name": "John",
            "Surname": "Lemon",
            "SexType": 1,
            "Initials": "JL",
            "DateOfBirth": "1958-08-02T00:00:00",
            "Mobile": "+444 895 523 411",
            "Telephone": "+444 525 111 555",
            "EmailAddress": "<john.lemon@test.com>",
            "WorkEmailAddress": "<john.lemon@mywork.com>",
            "Address": {
                "Address1": "Studio 99",
                "Address2": "Backlok Street",
                "Address3": "Camden",
                "City": "London",
                "County": "",
                "PostCode": "N1 7NK",
                "Country": "United Kingdom"
            }
        },
        "Key": "efdc81efac0fd1a7f7b1833697a3ec3b",
        "StartDate": "2018-06-11T00:00:00",
        "EstimatedEndDate": "2018-06-15T00:00:00",
        "EndDate": "2018-06-15T00:00:00",
        "AbsenceStatusCode": 2,
        "AbsenceStatusName": "Closed",
        "QuestionnaireStatusCode": 0,
        "QuestionnaireStatusName": "Not sent",
        "LostWork": {
            "Hours": 32,
            "Days": 4
        },
        "Reason": "Brain Tumour",
        "AccidentAtWork": false,
        "ReasonSharedWithEmployer": true
    }
}
```
