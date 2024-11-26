---
layout: page
title: DepartmentData
nav_order: 28
parent: Objects and data types
---

# DepartmentData

Contains the information about the company department.

## Properties

| Key | string |     |
| --- | --- | --- |
| Name | string |     |
| Divisions | DivisionData\[\] |     |
| ParentKey | int | The ID of the parent department, if it has one |

## JSON Example

```
{

"Key": "D123",

"Name": "HR"

}
```
