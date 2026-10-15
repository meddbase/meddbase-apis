---
layout: page
title: ActivePeriod
nav_order: 90
parent: Objects and data types
---

# ActivePeriod

The days in which a credit allowance can be used.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| FirstIncludedDay | string | The first day of the period, in the format `yyyy-MM-dd`. |
| LastIncludedDay | string (optional) | The last day of the period, in the format `yyyy-MM-dd`. It is not present if the period has no end. |

## JSON Example

```json
{
    "FirstIncludedDay": "2026-07-01",
    "LastIncludedDay": "2027-06-30"
}
```
