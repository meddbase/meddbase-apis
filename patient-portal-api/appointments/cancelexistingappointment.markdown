---
layout: page
title: CancelExistingAppointment
nav_order: 12
parent: Appointments
---

# CancelExistingAppointmentCancels the existing appointment and returns an invoice if any cancellation fee applies.## JavaScript library method```patientportal.appointment.cancelExistingAppointment({appointment: &lt;appointment&gt;});```## HTTP MethodGET## ****Url****/patientportalapi/appointment/cancel## URL Parameters| appointment | string | The key of the existing appointment provided by the API upon GetExistingAppointments. || --- | --- | --- |## ReturnInvoiceData## RemarksReturns null if no cancellation fee was applied.