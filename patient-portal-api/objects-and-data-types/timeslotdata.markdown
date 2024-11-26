---
layout: page
title: TimeSlotData
nav_order: 87
parent: Objects and data types
---

# TimeSlotData

## Properties

| Start | DateTime | Start time. |
| --- | --- | --- |
| Finish | DateTime | Finish time. |
| SiteKey | int | Key of the site the time slot is placed. |
| LocationKey | int | Key of the location the time slot is placed. |
| GrossPrice | decimal | The potential gross price of the appointment if booked using this time slot, might differ depending on the exact slot booked into. |
| NetPrice | decimal | The potential net price of the appointment if booked using this time slot, might differ depending on the exact slot booked into. |

## JSON Example

```
{

"Start": "2025-01-01T09:30:00",

"Finish": "2025-01-01T10:30:00",

"SiteKey": 123,

"LocationKey": 546,

"GrossPrice": 240,

"NetPrice": 200

}
```
