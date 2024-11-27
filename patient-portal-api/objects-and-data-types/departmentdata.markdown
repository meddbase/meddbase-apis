---
layout: page
title: DepartmentData
nav_order: 28
parent: Objects and data types
---

# DepartmentData

Contains the information about the company department.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Key | string |     |
| Name | string |     |
| Divisions | [DivisionData](../objects-and-data-types/divisiondata)[] |     |
| ParentKey | int | The ID of the parent department, if it has one |

## JSON Example

```json
{
    "Key": "D123",
    "Name": "HR"
}
```
