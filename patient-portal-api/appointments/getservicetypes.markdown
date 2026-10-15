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
    recall: <recall>,
    patientCourse: <patient-course>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/appointment/service-types` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| payer-type | string | Type of the payer provided by the API upon [GetPayerTypes](../appointments/getpayertypes). |
| appointment-type | string | Type of the appointment provided by the API upon [GetAppointmentTypes](../appointments/getappointmenttypes) |
| referral-types | bool (optional) | The key of the referral provided by the API upon [GetReferrals](../referrals/getreferrals).<br><br>Used to get service types for a specific referral. |
| patient | string (optional) | The key of the patient provided by the API upon section [Patients](../patients/patients).<br><br>Get the services specific for the patient. Default is the logged in patient. |
| referral | string (optional) | The key of the referral provided by the API upon [GetReferrals](../referrals/getreferrals).<br><br>Used to book an appointment for a specific referral. |
| recall | string (optional) | The key of the recall provided by the API upon method [GetRecalls](../recalls/getrecalls).<br><br>Used get service types for a specific recall. |
| patient-course | string (optional) | The key of the patient course provided by the API upon [GetPatientCourses](../courses/getpatientcourses).<br><br>Used to get service types that can be booked under a specific course. The course sets the payer and the prices, so `payer-type` is not used. Cannot be used with `referral`, `referral-types` or `recall`. See [Courses](../courses/courses). |

## Returns

[ServiceTypeData](../objects-and-data-types/servicetypedata)[]

## Remarks

If no service types are returned for the appointment type, either the appointment type does not allow additional services or no services exist in self book rule.
