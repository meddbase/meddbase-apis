---
layout: page
title: GetServiceTypes
nav_order: 4
parent: Anonymous Appointment Search
---

# GetServiceTypesGets service types (except) modules## JavaScript library method```patientportal.anonAppointment.getServiceTypes ({payerType: &lt;payer-type&gt;,appointmentType: <appointment-type});```## HTTP MethodGET## ****Url****/patientportalapi/anon-appointment/service-types## URL Parameters| payer-type | string | Type of the payer provided by the API upon GetPayerTypes. || --- | --- | --- || appointment-type | string | Type of the appointment provided by the API upon [GetAppointmentTypes](#_GetAppointmentTypes) |## Returns[ServiceTypeData](#_ServiceTypeData)\[\]## RemarksIf no service types are returned for the appointment type, either the appointment type does not allow additional services or no services exist in self book rule.