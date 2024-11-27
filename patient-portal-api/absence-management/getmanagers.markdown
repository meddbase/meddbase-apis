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

## Returns

[PatientDemographicData](../objects-and-data-types/patientdemographicdata)[]

## Returned JSON

```json
{
    "status": "ok",
    "result": [
        {
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
        }
    ]
}
```
