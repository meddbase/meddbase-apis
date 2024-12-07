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

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| absence-data | [AbsenceData](../objects-and-data-types/absencedata) | The [AbsenceData](../objects-and-data-types/absencedata) object received from a call to the [GetAbsence](../absence-management/getabsence) method. |

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
