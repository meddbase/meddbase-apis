---
layout: page
title: Anonymous Appointment Booking
nav_order: 9
parent: Patient Portal API
---

# Anonymous Appointment Booking

The previous section [Anonymous Appointment Search](../anonymous-appointment-search/anonymous-appointment-search) is used to find an available slot. This section allows the patient to book an appointment quickly without dealing with the standard [RegisterPatient](../authentication/registerpatient) process.

The workflow is:

- find an available slot via [GetProposedAppointments](../anonymous-appointment-search/getproposedappointments)
- register the patient with minimum demographics via [RegisterPatient](../anonymous-appointment-booking/registerpatient)
  - use SessionId for further communication
- verify 2FA ([ResendValidationCode](../anonymous-appointment-booking/resendvalidationcode), [SubmitValidationCode](../anonymous-appointment-booking/submitvalidationcode))
- book an appointment via [BookProposedAppointment](../anonymous-appointment-booking/bookproposedappointment)

Note that this workflow does not log the patient in. Once 2FA/booking completes you cannot use
