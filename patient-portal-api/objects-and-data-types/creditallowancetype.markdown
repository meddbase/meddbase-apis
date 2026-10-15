---
layout: page
title: CreditAllowanceType
nav_order: 97
parent: Objects and data types
---

# CreditAllowanceType

The type of a credit allowance. In JSON it is the name of the value, as a string.

## Values

| Value | Description |
|:------|:------------|
| Fixed | A fixed number of credits for each service. |
| FixedGroup | One pool of credits that the services share. |
| Interval | No fixed number of credits. Each service can be used again after a minimum interval. |
| IntervalGroup | No fixed number of credits. The services share the minimum interval. |
| Renewal | A number of credits for each service. The credits renew. |
| RenewalGroup | One pool of credits that the services share. The credits renew. |

## Fields of the allowance

The type defines which fields of [CreditAllowanceData](../objects-and-data-types/creditallowancedata) and [CourseAllowanceData](../objects-and-data-types/courseallowancedata) are present:

| Type | PoolCredits | Credits of a service | RenewalPeriod | MinimumInterval |
|:-----|:------------|:---------------------|:--------------|:----------------|
| Fixed | not present | present | not present | not present |
| FixedGroup | present | not present | not present | not present |
| Interval | not present | not present | not present | present |
| IntervalGroup | not present | not present | not present | present |
| Renewal | not present | present | present | not present |
| RenewalGroup | present | not present | present | not present |

For the types `Interval` and `IntervalGroup`, the balance of a patient has no `TotalOffered` and no `Remaining`.
