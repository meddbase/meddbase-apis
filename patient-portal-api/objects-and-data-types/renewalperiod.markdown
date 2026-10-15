---
layout: page
title: RenewalPeriod
nav_order: 107
parent: Objects and data types
---

# RenewalPeriod

How the credits of an allowance renew. It is used in [CreditAllowanceData](../objects-and-data-types/creditallowancedata) and [CourseAllowanceData](../objects-and-data-types/courseallowancedata).

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Years | int | The number of years in one renewal period. |
| Months | int | The number of months in one renewal period. |
| Days | int | The number of days in one renewal period. |
| MaximumNumberOfPeriods | int | The maximum number of renewal periods. |
| PerPatientStartDate | bool | True if each patient has a start date of their own for the renewal periods. |

## JSON Example

```json
{
    "Years": 1,
    "Months": 0,
    "Days": 0,
    "MaximumNumberOfPeriods": 1,
    "PerPatientStartDate": true
}
```
