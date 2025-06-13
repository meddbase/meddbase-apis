---
layout: page
title: Anonymous Appointment Search
nav_order: 8
parent: Patient Portal API
---

# Anonymous Appointment Search


This section provides methods for making anonymous (i.e. not authenticated) appointment searches. The methods are deliberately similar to the appointment search API documented in [Appointments](../appointments/appointments), but in these methods the `payer-type` parameter is expected to be a charge-band sign-up code. One or more charge-bands must be pre-configured in Meddbase to allow online sign-up and assigned a code before these methods can be used.

Methods in this section do not require a session id to be provided.

The results from an anonymous search can be used with the methods in [Anonymous Appointment Booking](../anonymous-appointment-booking/anonymous-appointment-booking) to book an appointment quickly without dealing with the standard [RegisterPatient](../authentication/registerpatient) process.
