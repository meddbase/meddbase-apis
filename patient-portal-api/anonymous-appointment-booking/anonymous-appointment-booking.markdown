---
layout: page
title: Anonymous Appointment Booking
nav_order: 9
parent: Patient Portal API
---

# Anonymous Appointment Booking
The previous section Anonymous Appointment Search is used to find an available slot. This section allows the patient to book an appointment quickly without dealing with the standard 5.10 RegisterPatient process.The workflow is:- find an available slot via GetProposedAppointments- register the patient with minimum demographics via 12.3 RegisterPatient  - use SessionId for further communication- verify 2FA (ResendValidationCode, SubmitValidationCode)- book an appointment via BookProposedAppointmentNote that this workflow does not log the patient in. Once 2FA/booking completes you cannot use