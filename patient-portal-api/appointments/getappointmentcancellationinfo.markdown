---
layout: page
title: GetAppointmentCancellationInfo
nav_order: 11
parent: Appointments
---

# GetAppointmentCancellationInfoReturns information about cancellation. The client should call this method when the user wants to cancel an appointment. The user will receive information about fees and any important conditions for the cancellation.## JavaScript library method```patientportal.appointment.getAppointmentCancellationInfo({appointment: &lt;appointment&gt;});```## HTTP MethodGET## ****Url****/patientportalapi/appointment/cancellation-info## URL Parameters| appointment | string | The key of the existing appointment provided by the API upon GetExistingAppointments. || --- | --- | --- |## ReturnAppointmentCancellationData