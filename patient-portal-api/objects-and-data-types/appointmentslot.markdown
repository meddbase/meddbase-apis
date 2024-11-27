---
layout: page
title: AppointmentSlot
nav_order: 9
parent: Objects and data types
---

# AppointmentSlot

Information about the appointment slot that the booking system needs to book the appointment.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Type | string | Type of appointment. |
| Start | DateTime | Start time. |
| Finish | DateTime | Finish time. |
| SiteKey | int | Key of the site the appointment is placed. |
| LocationKey | int | Key of the location within the site. |
| ResourceKey | int | Key of resources (stuff, rooms, etc.). Used for booking. |

## JSON Example

```json
{
    "Type": "VC",
    "Start": "2013-08-07T09:30:00",
    "Finish": "2013-08-07T10:30:00",
    "SiteKey": 123,
    "LocationKey": 546,
    "ResourceKey": 468
}
```
