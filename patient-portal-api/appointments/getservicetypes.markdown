---
layout: page
title: GetServiceTypes
nav_order: 3
parent: Appointments
---

# GetServiceTypes

Gets service types (except) modules

## JavaScript library method

```javascript
patientportal.appointment.getServiceTypes({
    payerType: <payer-type>,
    appointmentType: <appointment-type>,
    referralTypes: <referral-types>,
    patient: <patient>,
    referral: <referral>,
    recall: <recall>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/appointment/service-types` |

## URL Parameters

| payer-type | string | Type of the payer provided by the API upon GetPayerTypes. |
| --- | --- | --- |
| appointment-type | string | Type of the appointment provided by the API upon [GetAppointmentTypes](#_GetAppointmentTypes) |
| referral-types | bool (optional) | The key of the referral provided by the API upon GetReferrals.<br><br>Used to get service types for a specific referral. |
| patient | string (optional) | The key of the patient provided by the API upon section Patients.<br><br>Get the services specific for the patient. Default is the logged in patient. |
| referral | string (optional) | The key of the referral provided by the API upon GetReferrals.<br><br>Used to book an appointment for a specific referral. |
| recall | string (optional) | The key of the recall provided by the API upon method GetRecalls.<br><br>Used get service types for a specific recall. |

## Returns

[ServiceTypeData](#_ServiceTypeData)\[\]

## Remarks

If no service types are returned for the appointment type, either the appointment type does not allow additional services or no services exist in self book rule.
