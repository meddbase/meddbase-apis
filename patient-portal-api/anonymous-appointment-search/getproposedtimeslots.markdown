---
layout: page
title: GetProposedTimeSlots
nav_order: 7
parent: Anonymous Appointment Search
---

# GetProposedTimeSlots
## Gets proposed time slots according to given filters

## JavaScript library method

```javascript
patientportal.anonAppointment.getProposedTimeSlots({
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

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/anon-appointment/proposed-time-slots` |

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
            <td>Type of the appointment provided by the API upon <a href="../anonymous-appointment-search/getappointmenttypes">GetAppointmentTypes</a>.</td>
        </tr>
        <tr>
            <td>clinician</td>
            <td>int (optional)</td>
            <td>Clinician filter. Identifier provide by the API upon <a href="../anonymous-appointment-search/getclinicians">GetClinicians</a>. Allow 0 for any clinician.</td>
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
            <td>Site filter. Identifier provide by the API upon <a href="../anonymous-appointment-search/getsites">GetSites</a>. Allow 0 for any site.</td>
        </tr>
        <tr>
            <td>location</td>
            <td>int (optional)</td>
            <td>Location filter. Identifier provide by the API upon <a href="../anonymous-appointment-search/getsites">GetSites</a>. Allow 0 for any location.</td>
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
            <td><a href="../objects-and-data-types/localdatetime">LocalDateTime</a></td>
            <td>The end date/time for the search (exclusive).</td>
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
            <td>string “HH:mm” (optional)</td>
            <td>Time filter for the appointment start time. E.g 09:30.</td>
        </tr>
        <tr>
            <td>time-to</td>
            <td>string “HH:mm” (optional)</td>
            <td>Time filter for the appointment finish time. E.g 11:00.</td>
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
            <td>patient</td>
            <td>string (optional)</td>
            <td>
                <p>The key of the patient provided by the API upon section <a href="../patients/patients">Patients</a>.</p>
                <p>Used to book an appointment for a different patient within your company. Default is the logged in
                    patient.</p>
            </td>
        </tr>
        <tr>
            <td>referral</td>
            <td>string (optional)</td>
            <td>
                <p>The key of the referral provided by the API upon <a href="../referrals/getreferrals">GetReferrals</a>.</p>
                <p>Used to book an appointment for a specific referral.</p>
            </td>
        </tr>
        <tr>
            <td>recall</td>
            <td>string (optional)</td>
            <td>
                <p>The key of the recall provided by the API upon method <a href="../recalls/getrecalls">GetRecalls</a>.</p>
                <p>Used to book an appointment for a specific recall.</p>
            </td>
        </tr>
    </tbody>
</table>

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| modules | [AppointmentModuleData](../objects-and-data-types/appointmentmoduledata)[] (optional) | Selection of modules and additional services provided by the API upon [GetAppointmentTypes](../anonymous-appointment-search/getappointmenttypes). |
| services | [ServiceData](../objects-and-data-types/servicedata)[] (optional) | Selection of services provided by [GetServices](../anonymous-appointment-search/getservices) |

## Returns

[TimeSlotsData](../objects-and-data-types/timeslotsdata)

## Remarks

The server sorts the result by day and time of the appointment (the soonest appointment first).
