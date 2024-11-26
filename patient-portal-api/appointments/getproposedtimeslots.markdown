---
layout: page
title: GetProposedTimeSlots
nav_order: 19
parent: Appointments
---

# GetProposedTimeSlots

## Gets proposed time slots according to given filters

## JavaScript library method

```javascript
patientportal.appointment.getProposedTimeSlots({
    appointmentType: <appointment-type>,
    clinician: <clinician>,
    clinicianSex: <clinician-sex>,
    site: <site>,
    location: <location>,
    fromDate: <from-date>,
    toDate: <to-date>,
    timePreference: <time-preference>,
    timeFrom: <time-from>,
    timeTo: <time-to>,
    payerType: <payer-type>,
    patient: <patient>,
    referral: <referral>,
    recall: <recall>,
    modules: <modules>,
    services: <services>
});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/appointment/proposed-time-slots

## URL Parameters

<table><tbody><tr><th><p>appointment-type</p></th><th><p>string</p></th><th><p>Type of the appointment provided by the API upon GetAppointmentTypes.</p></th></tr><tr><td><p>clinician</p></td><td><p>int (optional)</p></td><td><p>Clinician filter. Identifier provide by the API upon GetClinicians. Allow 0 for any clinician.</p></td></tr><tr><td><p>clinician-sex</p></td><td><p>int (optional)</p></td><td><p>Clinician’s gender filter:</p><ul><li>0 = any sex</li><li>1 = male</li><li>2 = female</li></ul></td></tr><tr><td><p>site</p></td><td><p>int (optional)</p></td><td><p>Site filter. Identifier provide by the API upon GetSites. Allow 0 for any site.</p></td></tr><tr><td><p>location</p></td><td><p>int (optional)</p></td><td><p>Location filter. Identifier provide by the API upon GetSites. Allow 0 for any location.</p></td></tr><tr><td><p>from-date</p></td><td><p>LocalDateTime (optional)</p></td><td><p>Filters appointments on or after provided date/time (inclusive).</p><p>The parameter is a local date/time on a site. If you search across multiple sites in different time zones the search looks for the local date/time at each site.</p></td></tr><tr><td><p>to-date</p></td><td><p>LocalDateTime</p></td><td><p>The end date/time for the search (exclusive).</p></td></tr><tr><td><p>time-preference</p></td><td><p>int (optional)</p></td><td><p>Preferred time filter:</p><ul><li>0 = any time</li><li>1 = Morning 00:00 – 12:00</li><li>2 = Afternoon 12:00 – 00:00</li></ul><p>Note this parameter is ignored if any from time-from or time-to are provided.</p></td></tr><tr><td><p>time-from</p></td><td><p>string “HH:mm”</p><p>(optional)</p></td><td><p>Time filter for the appointment start time. E.g 09:30.</p></td></tr><tr><td><p>time-to</p></td><td><p>string “HH:mm”</p><p>(optional)</p></td><td><p>Time filter for the appointment finish time. E.g 11:00.</p></td></tr><tr><td><p>payer-type</p></td><td><p>string</p><p>(optional)</p></td><td><p>Type of the payer provided by the API upon GetPayerTypes.</p></td></tr><tr><td><p>patient</p></td><td><p>string (optional)</p></td><td><p>The key of the patient provided by the API upon section Patients.</p><p>Used to book an appointment for a different patient within your company. Default is the logged in patient.</p></td></tr><tr><td><p>referral</p></td><td><p>string (optional)</p></td><td><p>The key of the referral provided by the API upon GetReferrals.</p><p>Used to book an appointment for a specific referral.</p></td></tr><tr><td><p>recall</p></td><td><p>string (optional)</p></td><td><p>The key of the recall provided by the API upon method GetRecalls.</p><p>Used to book an appointment for a specific recall.</p></td></tr></tbody></table>

## POST Parameters

| modules | AppointmentModuleData\[\]<br><br>(optional) | Selection of modules and additional services provided by the API upon GetAppointmentTypes. |
| --- | --- | --- |
| services | [ServiceData](#_ServiceData)\[\]<br><br>(optional) | Selection of services provided by [GetServices](#_GetServices) |

## Returns

[TimeSlotsData](#_TimeSlotsData)

## Remarks

The server sorts the result by day and time of the appointment (the closer appointment first).
