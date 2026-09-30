---
layout: page
title: CreditAllowanceData
nav_order: 96
parent: Objects and data types
---

# CreditAllowanceData

A credit allowance of a course that is not bought yet. It shows what the course gives. It has no balances. It is used in [CourseData](../objects-and-data-types/coursedata). For a course that the patient has bought, see [CourseAllowanceData](../objects-and-data-types/courseallowancedata).

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Type | [CreditAllowanceType](../objects-and-data-types/creditallowancetype) | The type of the allowance. It defines which of the optional fields are present. |
| PoolCredits | int (optional) | The number of credits in the shared pool. It is present for the types `FixedGroup` and `RenewalGroup`. |
| RenewalPeriod | [RenewalPeriod](../objects-and-data-types/renewalperiod) (optional) | How the credits renew. It is present for the types `Renewal` and `RenewalGroup`. |
| MinimumInterval | [PeriodData](../objects-and-data-types/perioddata) (optional) | The minimum time between two uses. It is present for the types `Interval` and `IntervalGroup`. |
| ActivePeriod | [ActivePeriod](../objects-and-data-types/activeperiod) | The days in which the allowance can be used. |
| Services | [CreditServiceData](../objects-and-data-types/creditservicedata)[] | The services that the allowance covers. |

## JSON Example

```json
{
    "Type": "FixedGroup",
    "PoolCredits": 10,
    "ActivePeriod": {
        "FirstIncludedDay": "2026-07-01"
    },
    "Services": [
        {
            "ServiceKey": 501,
            "ServiceName": "Physiotherapy",
            "PublicNotes": "",
            "ServiceType": {
                "Code": "A",
                "Name": "Appointment"
            }
        },
        {
            "ServiceKey": 502,
            "ServiceName": "Massage",
            "PublicNotes": "",
            "ServiceType": {
                "Code": "A",
                "Name": "Appointment"
            }
        }
    ]
}
```
