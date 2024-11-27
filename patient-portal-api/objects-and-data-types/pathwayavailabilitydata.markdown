---
layout: page
title: PathwayAvailabilityData
nav_order: 55
parent: Objects and data types
---

# PathwayAvailabilityData

Availability data for a pathway definition

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| IsAvailable | bool | Availability Boolean for the pathway definition |
| Error | string | Reason for not being available. |

## JSON Example

```json
{
    "Error": "Maximum instances of pathways already running.",
    "IsAvailable": false
}
```
