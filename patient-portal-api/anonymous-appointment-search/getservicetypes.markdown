---
layout: page
title: GetServiceTypes
nav_order: 4
parent: Anonymous Appointment Search
---

# GetServiceTypes

Gets service types (except) modules

## JavaScript library method

```javascript
patientportal.anonAppointment.getServiceTypes({
    payerType: <payer-type>,
    appointmentType: <appointment-type
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/anon-appointment/service-types` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| payer-type | string | The signup code of a chargeband, that will provide eligibility and price information for the search. |
| appointment-type | string | Type of the appointment provided by the API upon [GetAppointmentTypes](../anonymous-appointment-search/getappointmenttypes) |

## Returns

[ServiceTypeData](../objects-and-data-types/servicetypedata)[]

## Remarks

If no service types are returned for the appointment type, either the appointment type does not allow additional services or no services exist in self book rule.
