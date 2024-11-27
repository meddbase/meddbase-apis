---
layout: page
title: PatientAbsenceOverviewData
nav_order: 56
parent: Objects and data types
---

# PatientAbsenceOverviewData

A small overview object containing the patient’s Bradford Factor score and a flag indicating whether they’re currently absent or not.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Key | string | The key of the patient. |
| IsCurrentlyAbsent | bool | A flag indicating whether the patient is currently absent or not. |
| BradfordFactor | int | The Bradford factor score for the patient for the time-period specified, or if not time-period is specified, the last 52-week period. |

## JSON Example

```json
{
    "BradfordFactor": 24,
    "IsCurrentlyAbsent": true,
    "Key": "83075be08d41fd6096c3c53bc8c4bda7"
}
```
