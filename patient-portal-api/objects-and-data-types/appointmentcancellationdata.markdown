---
layout: page
title: AppointmentCancellationData
nav_order: 6
parent: Objects and data types
---

# AppointmentCancellationData

Appointment cancellation information.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| AppointmentKey | string | Key of the appointment. |
| Fee | decimal | Cancellation fee that the patient must pay. |
| Detail | string | Any information about the cancellation. |

## JSON Example

```
{

"AppointmentKey": "apt54898",

"Fee": 30,

"Detail": "Cancellations within 8 to 21 days before appointment date will incur a 50% cancellation fee, between 0 and 7 days will incur a 100% cancellation fee."

}
```
