---
layout: page
title: GetProposedAppointments
nav_order: 6
parent: Anonymous Appointment Search
---

# GetProposedAppointments
Gets proposed appointments according given filters.

## JavaScript library method

```javascript
patientportal.appointment.getProposedAppointments({
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
    modules: <modules>,
    payerType: <payer-type>,
    numberOfResults: <number-of-results>
});
```

## HTTP Method

POST

## ****Url****

/patientportalapi/appointment/proposed

## URL Parameters

<table><tbody><tr><th><p>appointment-type</p></th><th><p>string</p></th><th><p>Type of the appointment provided by the API upon GetAppointmentTypes.</p></th></tr><tr><td><p>clinician</p></td><td><p>int (optional)</p></td><td><p>Clinician filter. Identifier provide by the API upon GetClinicians. Allow 0 for any clinician.</p></td></tr><tr><td><p>clinician-sex</p></td><td><p>int (optional)</p></td><td><p>Clinician’s gender filter:</p><ul><li>0 = any sex</li><li>1 = male</li><li>2 = female</li></ul></td></tr><tr><td><p>site</p></td><td><p>int (optional)</p></td><td><p>Site filter. Identifier provide by the API upon GetSites. Allow 0 for any site.</p></td></tr><tr><td><p>location</p></td><td><p>int (optional)</p></td><td><p>Location filter. Identifier provide by the API upon GetSites. Allow 0 for any location.</p></td></tr><tr><td><p>from-date</p></td><td><p>LocalDateTime (optional)</p></td><td><p>Filters appointments on or after provided date/time (inclusive).</p><p>The parameter is a local date/time on a site. If you search across multiple sites in different time zones the search looks for the local date/time at each site.</p></td></tr><tr><td><p>to-date</p></td><td><p>LocalDateTime (optional)</p></td><td><p>The end date/time for the search (exclusive). If not provided the API is looking for days/months into the future to satisfy the requested number-of-results. This may take some time. If you need to get slots for a specific day only it is recommended to provide to-date to make the request quick.</p></td></tr><tr><td><p>time-preference</p></td><td><p>int (optional)</p></td><td><p>Preferred time filter:</p><ul><li>0 = any time</li><li>1 = Morning 00:00 – 12:00</li><li>2 = Afternoon 12:00 – 00:00</li></ul><p>Note this parameter is ignored if any from time-from or time-to are provided.</p></td></tr><tr><td><p>time-from</p></td><td><p>string “HH:ss”</p><p>(optional)</p></td><td><p>Time filter for the appointment start time. E.g 09:30.</p></td></tr><tr><td><p>time-to</p></td><td><p>string “HH:ss”</p><p>(optional)</p></td><td><p>Time filter for the appointment finish time. E.g 11:00.</p></td></tr><tr><td><p>from-date</p></td><td><p>DateTime (optional)</p></td><td><p>Filters appointments on or after this date.</p><p>Note: Only day is accepted. Time is ignored.</p></td></tr><tr><td><p>time-preference</p></td><td><p>int (optional)</p></td><td><p>Preferred time filter:</p><ul><li>0 = any time</li><li>1 = Morning</li><li>2 = Afternoon</li></ul></td></tr><tr><td><p>payer-type</p></td><td><p>String</p><p>(Optional)</p></td><td><p>The signup code of a chargeband, that will provide eligibility and price information for the search.</p></td></tr><tr><td><p>number-of-results</p></td><td><p>Int (optional)</p></td><td><p>Required number of proposed slots. Value must be in a range 1 – 100.</p></td></tr></tbody></table>

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| modules | AppointmentModuleData\[\]<br><br>(optional) | Selection of modules and additional services provided by the API upon GetAppointmentTypes. |
| services | [ServiceData](#_ServiceData)\[\]<br><br>(optional) | Selection of services provided by [GetServices](#_GetServices) |

## Returns

AppointmentData\[\]

## Remarks

The server sorts the result by day and time of the appointment (the closer appointment first).
