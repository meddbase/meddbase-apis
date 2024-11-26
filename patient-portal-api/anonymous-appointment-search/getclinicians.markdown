---
layout: page
title: GetClinicians
nav_order: 3
parent: Anonymous Appointment Search
---

# GetClinicians
Gets possible clinicians/doctors for the specific appointment type.

## JavaScript Library

```javascript
patientportal.anonAppointment.getClinicians({
   appointmentType: 'appointment-type',
   sites: 'sites',
   locations: 'locations',
   payerType: 'payer-type',
   patient: 'patient',
   referral: 'referral',
   recall: 'recall'
});
```

## HTTP Method

| Verb | URL                                            |
|:-----|:-----------------------------------------------|
| POST | `/patientportalapi/anon-appointment/clinicians`|

## URL Parameters

| Parameter        | Type   | Required | Description                                                                                          |
|:-----------------|:-------|:---------|:-----------------------------------------------------------------------------------------------------|
| appointment-type | string | Yes      | Type of the appointment provided by the API upon GetAppointmentTypes.                                |
| payer-type       | string | Yes      | The signup code of a chargeband, that will provide eligibility and price information for the search. |

## POST Parameters

| Parameter   | Type                                                 | Required | Description                                                                                                                                                                          |
|:------------|:-----------------------------------------------------|:---------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sites       | int\[\]                                              | No       | Sites filter. Array of identifiers provide by the API upon GetSites.<br/><br/>Null or empty for any sites.                                                                             |
| locations   | int\[\]                                              | No       | Locations filter. Array of identifiers provide by the API upon GetSites.<br/><br/>Null or empty for any locations.                                                                     |
| modules     | [AppointmentModuleData](#_AppointmentModuleData)\[\] | No       | Selection of modules and additional services provided by the API upon GetAppointmentTypes.<br/><br/>Available clinicians will be filtered according to availability of the specified modules. |

## Returns

ClinicianData\[\]
