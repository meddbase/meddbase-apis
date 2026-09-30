---
layout: page
title: PatientCourseData
nav_order: 100
parent: Objects and data types
---

# PatientCourseData

A course that a patient has bought, with the credit balances. It has all the properties of [PatientCourseOverviewData](../objects-and-data-types/patientcourseoverviewdata) and the properties `CanBookOnline`, `Expiration` and `CreditAllowances`.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Key | string | Key of the patient course. Use it in the `patient-course` parameter. |
| CourseKey | string | Key of the course that was bought. Use it in the `course` parameter of [GetCourse](../courses/getcourse). |
| Code | string | Code of the course. |
| Name | string | Name of the course. |
| PublicNotes | string | Notes about the course for the patient. |
| FirstIncludedDay | string | The first day of the patient course, in the format `yyyy-MM-dd`. |
| LastIncludedDay | string | The last day of the patient course, in the format `yyyy-MM-dd`. |
| Status | [PatientCourseState](../objects-and-data-types/patientcoursestate) | The status of the patient course. |
| CanBookOnline | bool | True if at least one service of the course can be booked online. It is always false if `Status` is not `Active`. |
| Expiration | [PeriodData](../objects-and-data-types/perioddata) | How long the course is valid after its start date. All the values are 0 if the course does not expire. |
| CreditAllowances | [CourseAllowanceData](../objects-and-data-types/courseallowancedata)[] | The credits of the course, with the balances of the patient. |

## JSON Example

```json
{
    "Key": "8ebb55f10382d73e494e7207d1bd7272",
    "CourseKey": "c31a0f7e2b94d5581e6f70a3b2c49d10",
    "Code": "EHP",
    "Name": "Executive Health Programme",
    "PublicNotes": "Annual health programme.",
    "FirstIncludedDay": "2026-07-01",
    "LastIncludedDay": "2027-06-30",
    "Status": "Active",
    "CanBookOnline": true,
    "Expiration": {
        "Years": 1,
        "Months": 0,
        "Days": 0
    },
    "CreditAllowances": [
        {
            "Type": "Fixed",
            "ActivePeriod": {
                "FirstIncludedDay": "2026-07-01",
                "LastIncludedDay": "2027-06-30"
            },
            "Balance": {
                "TotalOffered": 6,
                "Used": 2,
                "Booked": 1,
                "Remaining": 3
            },
            "NextAvailableOn": "2026-09-30",
            "Services": [
                {
                    "ServiceKey": 501,
                    "ServiceName": "Physiotherapy",
                    "Credits": 6,
                    "PublicNotes": "",
                    "ServiceType": {
                        "Code": "A",
                        "Name": "Appointment"
                    },
                    "AppointmentType": {
                        "Key": "PHYS",
                        "Name": "Physiotherapy session"
                    }
                }
            ]
        }
    ]
}
```
