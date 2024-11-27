---
layout: page
title: GetServices
nav_order: 5
parent: Anonymous Appointment Search
---

# GetServices

Gets available services

## JavaScript library method

```javascript
patientportal.anonappointment.getServices({
    payerType: <payer-type>,
    appointmentType: <appointment-type>,
    serviceType: <service-type>,
    serviceName:<service-name>,
    pageSortColumn: <page-sort-column>,
    pageSortDescending: <page-sort-descending>,
    pageNumber: <page-number>,
    pageSize: <page-size>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/anon-appointment/services` |

## URL Parameters

<table><tbody><tr><th><p>payer-type</p></th><th colspan="2"><p>string</p></th><th><p>Type of the payer provided by the API upon GetPayerTypes.</p></th></tr><tr><td><p>appointment-type</p></td><td colspan="2"><p>string</p></td><td><p>Type of the appointment provided by the API upon <a href="#_GetAppointmentTypes">GetAppointmentTypes</a></p></td></tr><tr><td><p>service-type</p></td><td colspan="2"><p>string</p><p>(optional)</p></td><td><p>Key of the service type to filter services by, provided by <a href="#_GetServiceTypes">GetServiceTypes</a></p></td></tr><tr><td><p>service-name</p></td><td colspan="2"><p>string</p><p>(optional)</p></td><td><p>Name of service to filter services by.</p></td></tr><tr><td><p>page-sort-column</p></td><td><p>int (optional)</p></td><td colspan="2"><p>The column index to sort the result:</p><ul><li>0 – Name</li><li>1 – Code</li><li>2- Service Type</li><li>3- ServiceId</li></ul><p>Default: 0,2</p></td></tr><tr><td><p>page-sort-descending</p></td><td><p>int (optional)</p></td><td colspan="2"><p>True to sort result descending. Default false.</p></td></tr><tr><td><p>page-number</p></td><td><p>int (optional)</p></td><td colspan="2"><p>Required page number. Default 1.</p></td></tr><tr><td><p>page-size</p></td><td><p>int (optional)</p></td><td colspan="2"><p>Required page size. Default 10. Minimum 5. Maximum 50.</p></td></tr></tbody></table>

## Returns

[ServiceData](../objects-and-data-types/servicedata)[]

## Remarks

If no services are returned for the appointment type, either the appointment type does not allow additional services or no services exist in self book rule.
