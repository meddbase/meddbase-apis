---
layout: page
title: CreditBalance
nav_order: 98
parent: Objects and data types
---

# CreditBalance

The credits of a patient for an allowance that does not renew. It is used in [CourseAllowanceData](../objects-and-data-types/courseallowancedata).

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| TotalOffered | int (optional) | The number of credits that the allowance gives. It is not present for the types `Interval` and `IntervalGroup`. |
| Used | int | The number of credits that are used. |
| Booked | int | The number of credits that are booked, but not used yet. |
| Remaining | int (optional) | The number of credits that are left. It is not present for the types `Interval` and `IntervalGroup`. |

## JSON Example

```json
{
    "TotalOffered": 6,
    "Used": 2,
    "Booked": 1,
    "Remaining": 3
}
```
