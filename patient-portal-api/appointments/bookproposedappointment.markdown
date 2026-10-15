---
layout: page
title: BookProposedAppointment
nav_order: 8
parent: Appointments
---

# BookProposedAppointment

Books and returns the new appointment. Returned appointment contains the amount owned by the patient.

## JavaScript library method

```javascript
patientportal.appointment.bookProposedAppointment({
    proposedAppointment: <proposedAppointment> ,
    patient: <patient>,
    referral: <referral>,
    recall: <recall>,
    patientCourse: <patient-course>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/appointment/book` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| patient | string (optional) | The key of the patient provided by the API upon section [Patients](../patients/patients).<br><br>Used to book an appointment for a different patient within your company. Default is the logged in patient. |
| referral | string (optional) | The key of the referral provided by the API upon [GetReferrals](../referrals/getreferrals).<br><br>Used to book an appointment for a specific referral. |
| recall | string (optional) | The key of the recall provided by the API upon method [GetRecalls](../recalls/getrecalls).<br><br>Used to book an appointment for a specific recall. |
| patient-course | string (optional) | The key of the patient course provided by the API upon [GetPatientCourses](../courses/getpatientcourses).<br><br>Used to book the appointment under a course that the patient has bought. The course must be active and the appointment must be inside its dates. Cannot be used with `referral` or `recall`. See [Courses](../courses/courses). |

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| proposedAppointment | AppointmentData | The proposed appointment provided by the API upon [GetProposedAppointments](../appointments/getproposedappointments). |

## Returns

[AppointmentData](../objects-and-data-types/appointmentdata)

## Remarks

If the appropriate appointment is taken by another user in the meantime then an exception is thrown. See [Error handling](../error-handling/error-handling). If the response contains the invoice the client use the invoice number and unpaid part of invoice to provide payment.
