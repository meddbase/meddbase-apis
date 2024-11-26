---
layout: page
title: BookProposedAppointment
nav_order: 6
parent: Address Finder
---

# BookProposedAppointment

Creates the patient in our system and books an appointment. Returns the new appointment.

## JavaScript library method

```
patientportal.anonBooking.bookProposedAppointment({

proposedAppointment: &lt;proposedAppointment&gt;

});
```

## HTTP Method

POST

## ****Url****

/patientportalapi/anon-booking/book

## POST Parameters

| proposedAppointment | AppointmentData | The proposed appointment provided by the API upon GetProposedAppointments |
| --- | --- | --- |

## Returns

AppointmentData

## Remarks

If the appropriate appointment is taken by another user in a meanwhile the exception is throw. See Error handling.
