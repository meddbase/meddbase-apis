---
layout: page
title: GetAppointmentTypes
nav_order: 1
parent: Anonymous Appointment Search
---

# GetAppointmentTypesGets appointment types (e.g. Consultation, Health Screen, etc.) available for booking.## JavaScript library method```patientportal.anonAppointment.getAppointmentTypes({payerType: &lt;payer-type&gt;});```## HTTP MethodGET## ****Url****/patientportalapi/anon-appointment/types## URL Parameters| payer-type | string | The signup code of a chargeband, that will provide eligibility and price information for the search. || --- | --- | --- |## ReturnsAppointmentTypeData\[\]## RemarksIf no module is returned for the appointment type, it doesn’t contain modules and the booking process can continue without selecting the module.