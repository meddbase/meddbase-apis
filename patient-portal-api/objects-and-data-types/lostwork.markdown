---
layout: page
title: LostWork
nav_order: 44
parent: Objects and data types
---

# LostWork

A small object used in the [AbsenceData](../objects-and-data-types/absencedata) and [AbsenceOverview](../objects-and-data-types/absenceoverviewdata) to encapsulate the number of hours and days lost due to the patient’s absence. The **Hours** and **Days** in the object are separate, in that they do not mean that _the patient was absent for four days and 32 hours_, they mean that _the patient was absent for four days, which is equivalent to 32 hours_.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Hours | decimal (optional) | The number of hours that the patient was absent. |
| Days | decimal (optional) | The number of days that the patient was absent. |

## JSON Example

```
{

"Hours": 32,

"Days": 4

}
```
