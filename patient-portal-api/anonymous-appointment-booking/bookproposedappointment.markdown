---
layout: page
title: BookProposedAppointment
nav_order: 4
parent: Anonymous Appointment Booking
---

# BookProposedAppointment

Creates the patient in our system and books an appointment. Returns the new appointment.

## JavaScript library method

```javascript
patientportal.anonBooking.bookProposedAppointment({
    proposedAppointment: <proposedAppointment>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/anon-booking/book` |

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| proposedAppointment | [AppointmentData](../objects-and-data-types/appointmentdata) | The proposed appointment provided by the API upon GetProposedAppointments |

## Returns

[AppointmentData](../objects-and-data-types/appointmentdata)

## Remarks

If the appropriate appointment is taken by another user in a meanwhile the exception is throw. See Error handling.
