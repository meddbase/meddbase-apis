---
layout: page
title: GetAppointmentTypes
nav_order: 1
parent: Anonymous Appointment Search
---

# GetAppointmentTypes
Gets appointment types (e.g. Consultation, Health Screen, etc.) available for booking.

## JavaScript Library

```javascript
patientportal.anonAppointment.getAppointmentTypes({
    payerType: 'payer-type';
});
```

## HTTP Method

| Verb | URL                                       |
|:-----|:------------------------------------------|
| GET  | `/patientportalapi/anon-appointment/types`|

## URL Parameters

| Parameter  | Type   | Required | Description                                                                                          |
|:-----------|:-------|:---------|:-----------------------------------------------------------------------------------------------------|
| payer-type | string | Yes      | The signup code of a chargeband, that will provide eligibility and price information for the search. |

## Returns

AppointmentTypeData\[\]

{: .note }
> If no module is returned for the appointment type, it doesn't contain modules and the booking process can continue without selecting the module.
