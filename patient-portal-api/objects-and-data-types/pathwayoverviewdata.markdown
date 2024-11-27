---
layout: page
title: PathwayOverviewData
nav_order: 51
parent: Objects and data types
---

# PathwayOverviewData

Provides overview information about the pathway.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Key | string | The key of the pathway. |
| Number | string | The number of the pathway. |
| Name | string | The name of the pathway. |
| Patient | string | The name of the patient. |
| State | string | The current pathway state. |
| CurrentAction | string | The action that is currently active. |
| LastUpdate | DateTime | Last modification date. |
| DueDate | DateTime | The current active action due date. |

## JSON Example

```json
{
    "Key": "a1d3e2d1",
    "Number": "123",
    "Name": "Book & Arrive",
    "Patient": "Mr. Will Smith",
    "State": "In progress",
    "CurrentAction": "Book an appointment",
    "LastUpdate": "2015-03-13T14:22:12",
    "DueDate": "2015-03-13T14:52:30"
}
```
