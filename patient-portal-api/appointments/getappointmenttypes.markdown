---
layout: page
title: GetAppointmentTypes
nav_order: 2
parent: Appointments
---

# GetAppointmentTypes

Gets appointment types (e.g. Consultation, Health Screen, etc.) available for booking.

## JavaScript library method

```javascript
patientportal.appointment.getAppointmentTypes({
    payerType: <payer-type>,
    referralTypes: <referral-types>,
    patient: <patient>,
    referral: <referral>,
    recall: <recall>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/appointment/types` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| payer-type | string (optional) | Type of the payer provided by the API upon [GetPayerTypes](../appointments/getpayertypes). |
| referral-types | bool (optional) | True to return the list of appointment types the patient can be referred for. Otherwise false. Default false. |
| patient | string (optional) | The key of the patient provided by the API upon section [Patients](../patients/patients).<br><br>Used to book an appointment for a different patient within your company. Default is the logged in patient. |
| referral | string (optional) | The key of the referral provided by the API upon [GetReferrals](../referrals/getreferrals).<br><br>Used to book an appointment for a specific referral. |
| recall | string (optional) | The key of the recall provided by the API upon method [GetRecalls](../recalls/getrecalls).<br><br>Used to book an appointment for a specific recall. |

## Returns

[AppointmentTypeData](../objects-and-data-types/appointmenttypedata)[]

## Remarks

If no module is returned for the appointment type, it doesn’t contain modules and the booking process can continue without selecting the module.
