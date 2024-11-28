---
layout: page
title: RecallData
nav_order: 74
parent: Objects and data types
---

# RecallData

Provides information about the recall.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Key | string | The key of the recall. |
| Patient | [PersonDemographicData](../objects-and-data-types/persondemographicdata) | The patient data. |
| Reason | string | The reason for the recall. |
| AppointmentType | [AppointmentTypeData](../objects-and-data-types/appointmenttypedata) | The appointment type. |
| DueDate | [DateTime](../objects-and-data-types/datetime) | Recall due date. |
| Clinician | [ClinicianData](../objects-and-data-types/cliniciandata) | The clinician who triggered the recall. |

## JSON Example

```json
{
    "Key": "3bdd966cf6f9c0c6872ee0551da74c4d",
    "DueDate": "2017-03-14T00:00:00",
    "Reason": "Test",
    "AppointmentType": {
        "Key": "CN",
        "Name": "Consultation",
        "CancellationPolicy": "You will be charged at 50% of the full price if you cancel the appointment within 72 hours. You will be charged at 90% of the full price if you do not turn up.",
        "CanBookAppointment": true,
        "CanReferPatient": false,
        "TelemedicineOption": true,
        "CanAddServices": false
    },
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
    "Clinician": {
        "Key": 84,
        "FullName": "Dr. House"
    }
}
```
