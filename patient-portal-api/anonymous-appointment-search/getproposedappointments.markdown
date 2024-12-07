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

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/appointment/proposed` |

## URL Parameters

<table>
    <thead>
        <tr>
            <th style="text-align: left">Parameter</th>
            <th style="text-align: left">Type</th>
            <th style="text-align: left">Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>appointment-type</td>
            <td>string</td>
            <td>Type of the appointment provided by the API upon GetAppointmentTypes.</td>
        </tr>
        <tr>
            <td>clinician</td>
            <td>int (optional)</td>
            <td>Clinician filter. Identifier provide by the API upon GetClinicians. Allow 0 for any clinician.</td>
        </tr>
        <tr>
            <td>clinician-sex</td>
            <td>int (optional)</td>
            <td>
                <p>Clinician’s gender filter:</p>
                <ul>
                    <li>0 = any sex</li>
                    <li>1 = male</li>
                    <li>2 = female</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>site</td>
            <td>int (optional)</td>
            <td>Site filter. Identifier provide by the API upon GetSites. Allow 0 for any site.</td>
        </tr>
        <tr>
            <td>location</td>
            <td>int (optional)</td>
            <td>Location filter. Identifier provide by the API upon GetSites. Allow 0 for any location.</td>
        </tr>
        <tr>
            <td>from-date</td>
            <td><a href="../objects-and-data-types/localdatetime">LocalDateTime</a> (optional)</td>
            <td>
                <p>Filters appointments on or after provided date/time (inclusive).</p>
                <p>The parameter is a local date/time on a site. If you search across multiple sites in different time
                    zones the search looks for the local date/time at each site.</p>
            </td>
        </tr>
        <tr>
            <td>to-date</td>
            <td><a href="../objects-and-data-types/localdatetime">LocalDateTime</a> (optional)</td>
            <td>
                <p>The end date/time for the search (exclusive). If not provided the API is looking for days/months into
                    the future to satisfy the requested number-of-results. This may take some time. If you need to get
                    slots for a specific day only it is recommended to provide to-date to make the request quick.</p>
            </td>
        </tr>
        <tr>
            <td>time-preference</td>
            <td>int (optional)</td>
            <td>
                <p>Preferred time filter:</p>
                <ul>
                    <li>0 = any time</li>
                    <li>1 = Morning 00:00 – 12:00</li>
                    <li>2 = Afternoon 12:00 – 00:00</li>
                </ul>
                <p>Note this parameter is ignored if any from time-from or time-to are provided.</p>
            </td>
        </tr>
        <tr>
            <td>time-from</td>
            <td>string “HH:ss” (optional)</td>
            <td>Time filter for the appointment start time. E.g 09:30.</td>
        </tr>
        <tr>
            <td>time-to</td>
            <td>string “HH:ss” (optional)</td>
            <td>Time filter for the appointment finish time. E.g 11:00.</td>
        </tr>
        <tr>
            <td>from-date</td>
            <td><a href="../objects-and-data-types/datetime">DateTime</a> (optional)</td>
            <td>
                <p>Filters appointments on or after this date.</p>
                <p>Note: Only day is accepted. Time is ignored.</p>
            </td>
        </tr>
        <tr>
            <td>time-preference</td>
            <td>int (optional)</td>
            <td>
                <p>Preferred time filter:</p>
                <ul>
                    <li>0 = any time</li>
                    <li>1 = Morning</li>
                    <li>2 = Afternoon</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>payer-type</td>
            <td>string (optional)</td>
            <td>
                <p>The signup code of a chargeband, that will provide eligibility and price information for the search.
                </p>
            </td>
        </tr>
        <tr>
            <td>number-of-results</td>
            <td>int (optional)</td>
            <td>Required number of proposed slots. Value must be in a range 1 – 100.</td>
        </tr>
    </tbody>
</table>

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| modules | [AppointmentData](../objects-and-data-types/appointmentdata)[] (optional) | Selection of modules and additional services provided by the API upon GetAppointmentTypes. |
| services | [ServiceData](../objects-and-data-types/servicedata)[] (optional) | Selection of services provided by [GetServices](#_GetServices) |

## Returns

[AppointmentData](../objects-and-data-types/appointmentdata)[]

## Remarks

The server sorts the result by day and time of the appointment (the soonest appointment first).
