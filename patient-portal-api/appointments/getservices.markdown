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

GET

## ****Url****

/patientportalapi/appointment/services

## URL Parameters

<table><tbody><tr><th><p>payer-type</p></th><th colspan="2"><p>string</p></th><th><p>Type of the payer provided by the API upon GetPayerTypes.</p></th></tr><tr><td><p>appointment-type</p></td><td colspan="2"><p>string</p></td><td><p>Type of the appointment provided by the API upon <a href="#_GetAppointmentTypes">GetAppointmentTypes</a></p></td></tr><tr><td><p>service-type</p></td><td colspan="2"><p>string</p><p>(optional)</p></td><td><p>Key of the service type to filter services by, provided by <a href="#_GetServiceTypes">GetServiceTypes</a></p></td></tr><tr><td><p>service-name</p></td><td colspan="2"><p>string</p><p>(optional)</p></td><td><p>Name of service to filter services by.</p></td></tr><tr><td><p>referral-types</p></td><td colspan="2"><p>bool (optional)</p></td><td><p>The key of the referral provided by the API upon GetReferrals.</p><p>Used to get service types for a specific referral.</p></td></tr><tr><td><p>patient</p></td><td colspan="2"><p>string (optional)</p></td><td><p>The key of the patient provided by the API upon section Patients.</p><p>Get the services specific for the patient. Default is the logged in patient.</p></td></tr><tr><td><p>referral</p></td><td colspan="2"><p>string (optional)</p></td><td><p>The key of the referral provided by the API upon GetReferrals.</p><p>Used to book an appointment for a specific referral.</p></td></tr><tr><td><p>recall</p></td><td colspan="2"><p>string (optional)</p></td><td><p>The key of the recall provided by the API upon method GetRecalls.</p><p>Used get service types for a specific recall.</p></td></tr><tr><td><p>page-sort-column</p></td><td><p>int (optional)</p></td><td colspan="2"><p>The column index to sort the result:</p><ul><li>0 – Name</li><li>1 – Code</li><li>2- Service Type</li><li>3- ServiceId</li></ul><p>Default: 0,2</p></td></tr><tr><td><p>page-sort-descending</p></td><td><p>int (optional)</p></td><td colspan="2"><p>True to sort result descending. Default false.</p></td></tr><tr><td><p>page-number</p></td><td><p>int (optional)</p></td><td colspan="2"><p>Required page number. Default 1.</p></td></tr><tr><td><p>page-size</p></td><td><p>int (optional)</p></td><td colspan="2"><p>Required page size. Default 10. Minimum 5. Maximum 50.</p></td></tr></tbody></table>

## Returns

[ServiceData](#_ServiceData)\[\]

## Remarks

If no services are returned for the appointment type, either the appointment type does not allow additional services or no services exist in self book rule.
