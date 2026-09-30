---
layout: page
title: CourseAllowanceData
nav_order: 91
parent: Objects and data types
---

# CourseAllowanceData

A credit allowance of a patient course, with the balances of the patient. It is used in [PatientCourseData](../objects-and-data-types/patientcoursedata). For a course that is not bought yet, see [CreditAllowanceData](../objects-and-data-types/creditallowancedata).

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Type | [CreditAllowanceType](../objects-and-data-types/creditallowancetype) | The type of the allowance. It defines which of the optional fields are present. |
| PoolCredits | int (optional) | The number of credits in the shared pool. It is present for the types `FixedGroup` and `RenewalGroup`. |
| RenewalPeriod | [RenewalPeriod](../objects-and-data-types/renewalperiod) (optional) | How the credits renew. It is present for the types `Renewal` and `RenewalGroup`. |
| MinimumInterval | [PeriodData](../objects-and-data-types/perioddata) (optional) | The minimum time between two uses. It is present for the types `Interval` and `IntervalGroup`. |
| ActivePeriod | [ActivePeriod](../objects-and-data-types/activeperiod) | The days in which the allowance can be used. |
| Balance | [CreditBalance](../objects-and-data-types/creditbalance) (optional) | The credits of the patient. It is present when the credits do not renew. |
| Period | [PeriodBalance](../objects-and-data-types/periodbalance) (optional) | The credits of the patient in the current renewal period. It is present when the credits renew. |
| NextAvailableOn | string (optional) | The first day on which a new booking can use the allowance, in the format `yyyy-MM-dd`. It is not present when nothing is left to book. |
| Services | [CreditServiceData](../objects-and-data-types/creditservicedata)[] | The services that the allowance covers. |

## Remarks

Exactly one of `Balance` and `Period` is present.

When the active period of the allowance has ended, the balances do not show the credits that were spent.

## JSON Example

```json
{
    "Type": "Renewal",
    "RenewalPeriod": {
        "Years": 1,
        "Months": 0,
        "Days": 0,
        "MaximumNumberOfPeriods": 1,
        "PerPatientStartDate": true
    },
    "ActivePeriod": {
        "FirstIncludedDay": "2026-07-01",
        "LastIncludedDay": "2027-06-30"
    },
    "Period": {
        "TotalOffered": 1,
        "Used": 0,
        "Booked": 0,
        "Remaining": 1,
        "RenewsOn": "2027-07-01"
    },
    "NextAvailableOn": "2026-09-30",
    "Services": [
        {
            "ServiceKey": 501,
            "ServiceName": "Physiotherapy",
            "Credits": 1,
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
```
