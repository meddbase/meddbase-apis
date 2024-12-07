---
layout: page
title: GetSites
nav_order: 5
parent: Appointments
---

# GetSites

Gets possible sites for the specific appointment type. A site is a geographically-unique place. Each site may include additional 'locations', which are typically rooms at the site (Room 123, Surgery, etc.), but may also be geographically different places associated with the site (First floor, West wing, Building 3, etc.).

The API will only present you with locations which mean something to a user. So they're unlikely to get a choice about Room 1, 2, 3, etc. but they may get a choice about Site: My Bank, Location: Floor 1, Floor 50, Floor 100, etc.

## JavaScript library method

```javascript
patientportal.appointment.getSites({
    appointmentType: <appointment-type>,
    lat: <lat>,
    long: <long>,
    addressType: <address-type>,
    clinicians: <clinicians>,
    payerType: <payer-type>,
    patient: <patient>,
    referral: <referral>,
    recall: <recall>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/appointment/sites` |

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
            <td>lat</td>
            <td rowspan="2">
                <p>decimal (optional)</p>
            </td>
            <td rowspan="2">
                <p>Latitude and Longitude from GPS so server can sort sites by distance.</p>
                <p>
                    Latitudes and Longitudes are defined using numerals that have a precision to 6 decimal places.
                    For example, <code>lat=51.541743&amp;long=-0.13715</code> is a valid value.</p>
            </td>
        </tr>
        <tr>
            <td>long</td>
        </tr>
        <tr>
            <td>address-type</td>
            <td>int (optional)</td>
            <td>
                <p>Parameter specifies how the response should be sorted:</p>
                <ul>
                    <li>1 = Home address</li>
                    <li>2 = Work address</li>
                </ul>
                <p>The server uses this value only if the GPS coordinate is not provided.</p>
            </td>
        </tr>
        <tr>
            <td>payer-type</td>
            <td>string</td>
            <td>Type of the payer provided by the API upon GetPayerTypes.</td>
        </tr>
        <tr>
            <td>patient</td>
            <td>string (optional)</td>
            <td>
                <p>The key of the patient provided by the API upon section Patients.</p>
                <p>Used to book an appointment for a different patient within your company. Default is the logged in
                    patient.</p>
            </td>
        </tr>
        <tr>
            <td>referral</td>
            <td>string (optional)</td>
            <td>
                <p>The key of the referral provided by the API upon GetReferrals.</p>
                <p>Used to book an appointment for a specific referral.</p>
            </td>
        </tr>
        <tr>
            <td>recall</td>
            <td>string (optional)</td>
            <td>
                <p>The key of the recall provided by the API upon method GetRecalls.</p>
                <p>Used to book an appointment for a specific recall.</p>
            </td>
        </tr>
    </tbody>
</table>

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| clinicians | int[] (optional) | Clinicians filter. Array of identifiers provide by the API upon GetClinicians. Null or empty for any clinicians. |
| modules | [AppointmentModuleData](../objects-and-data-types/appointmentmoduledata)[] (optional) | Selection of modules and additional services provided by the API upon GetAppointmentTypes. Available sites will be filtered according to availability of the specified modules. |

## Returns

[SiteData](../objects-and-data-types/sitedata)[]

## Remarks

If no lat/long or addressType is provided the server sorts sites by the patient’s home address.
