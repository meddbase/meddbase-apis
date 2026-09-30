---
layout: page
title: PeriodBalance
nav_order: 104
parent: Objects and data types
---

# PeriodBalance

The credits of a patient in the current renewal period of an allowance that renews. It is used in [CourseAllowanceData](../objects-and-data-types/courseallowancedata).

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| TotalOffered | int | The number of credits that the allowance gives in the period. |
| Used | int | The number of credits that are used in the period. |
| Booked | int | The number of credits that are booked in the period, but not used yet. |
| Remaining | int | The number of credits that are left in the period. |
| RenewsOn | string (optional) | The day on which the credits renew, in the format `yyyy-MM-dd`. It is not present in the last period. |

## JSON Example

```json
{
    "TotalOffered": 1,
    "Used": 0,
    "Booked": 0,
    "Remaining": 1,
    "RenewsOn": "2027-07-01"
}
```
