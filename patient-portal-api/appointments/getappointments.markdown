---
layout: page
title: GetAppointments
nav_order: 10
parent: Appointments
---

# GetAppointments

Gets the patient’s appointments.

## JavaScript library method

```javascript
patientportal.appointment.getAppointments({
    patient: <patient>,
    appointmentTypeName: <appointment-type-name>,
    startFrom: <start-from>,
    startTo: <start-to>,
    case: <case>,
    pageSortColumn: <page-sort-column>,
    pageSortDescending: <page-sort-descending>,
    pageNumber: <page-number>,
    pageSize: <page-size>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/appointment/appointments` |

## URL Parameters

<table><tbody><tr><th><p>patient</p></th><th><p>string (optional)</p></th><th><p>The key of the patient provided by the API upon section Patients.</p><p>Default is undefined which returns appointments for all patients.</p></th></tr><tr><td><p>appointment-type-name</p></td><td><p>string (optional)</p></td><td><p>The appointment type name filter.</p></td></tr><tr><td><p>start-from</p></td><td><p>DateTime (optional)</p></td><td><p>The appointment start date filter.</p></td></tr><tr><td><p>start-to</p></td><td><p>DateTime (optional)</p></td><td><p>The appointment start date filter.</p></td></tr><tr><td><p>case</p></td><td><p>int (optional)</p></td><td><p>The case key for the appointment.</p></td></tr><tr><td><p>page-sort-column</p></td><td><p>int (optional)</p></td><td><p>The column index to sort the result:</p><ul><li>0 –Start date</li><li>1 – Appointment type name</li></ul><p>Default: 0</p></td></tr><tr><td><p>page-sort-descending</p></td><td><p>int (optional)</p></td><td><p>True to sort result descending. Default false.</p></td></tr><tr><td><p>page-number</p></td><td><p>int (optional)</p></td><td><p>Required page number. Default 1.</p></td></tr><tr><td><p>page-size</p></td><td><p>int (optional)</p></td><td><p>Required page size. Default 10. Minimum 5. Maximum 50.</p></td></tr></tbody></table>

## Returned JSON

```
{

"Items": \[

<list of AppointmentData>

\]

"TotalCount":24,

"CurrentPage":1,

"PageSize":10,

"SortColumn": 0,

"SortDescending": false

}
```
