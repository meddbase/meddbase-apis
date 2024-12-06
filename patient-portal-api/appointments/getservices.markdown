---
layout: page
title: GetServices
nav_order: 4
parent: Appointments
---

# GetServices

Gets available services

## JavaScript library method

```javascript
patientportal.appointment.getServices({
    payerType: <payer-type>,
    appointmentType: <appointment-type>,
    serviceType: <service-type>,
    serviceName:<service-name>,
    referralTypes: <referral-types>,
    patient: <patient>,
    referral: <referral>,
    recall: <recall>,
    pageSortColumn: <page-sort-column>,
    pageSortDescending: <page-sort-descending>,
    pageNumber: <page-number>,
    pageSize: <page-size>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/appointment/services` |

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
            <td>payer-type</td>
            <td>string</td>
            <td>Type of the payer provided by the API upon GetPayerTypes.</td>
        </tr>
        <tr>
            <td>appointment-type</td>
            <td>string</td>
            <td>
                <p>Type of the appointment provided by the API upon <a
                        href="#_GetAppointmentTypes">GetAppointmentTypes</a></p>
            </td>
        </tr>
        <tr>
            <td>service-type</td>
            <td>string (optional)</td>
            <td>
                <p>Key of the service type to filter services by, provided by <a
                        href="#_GetServiceTypes">GetServiceTypes</a></p>
            </td>
        </tr>
        <tr>
            <td>service-name</td>
            <td>string (optional)</td>
            <td>Name of service to filter services by.</td>
        </tr>
        <tr>
            <td>referral-types</td>
            <td>bool (optional)</td>
            <td>
                <p>The key of the referral provided by the API upon GetReferrals.</p>
                <p>Used to get service types for a specific referral.</p>
            </td>
        </tr>
        <tr>
            <td>patient</td>
            <td>string (optional)</td>
            <td>
                <p>The key of the patient provided by the API upon section Patients.</p>
                <p>Get the services specific for the patient. Default is the logged in patient.</p>
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
                <p>Used get service types for a specific recall.</p>
            </td>
        </tr>
        <tr>
            <td>page-sort-column</td>
            <td>int (optional)</td>
            <td>
                <p>The column index to sort the result:</p>
                <ul>
                    <li>0 – Name</li>
                    <li>1 – Code</li>
                    <li>2- Service Type</li>
                    <li>3- ServiceId</li>
                </ul>
                <p>Default: 0,2</p>
            </td>
        </tr>
        <tr>
            <td>page-sort-descending</td>
            <td>int (optional)</td>
            <td>True to sort result descending. Default false.</td>
        </tr>
        <tr>
            <td>page-number</td>
            <td>int (optional)</td>
            <td>Required page number. Default 1.</td>
        </tr>
        <tr>
            <td>page-size</td>
            <td>int (optional)</td>
            <td>Required page size. Default 10. Minimum 5. Maximum 50.</td>
        </tr>
    </tbody>
</table>

## Returns

[ServiceData](../objects-and-data-types/servicedata)[]

## Remarks

If no services are returned for the appointment type, either the appointment type does not allow additional services or no services exist in self book rule.
