---
layout: page
title: CreditServiceData
nav_order: 99
parent: Objects and data types
---

# CreditServiceData

A service that a credit allowance covers. It is used in [CreditAllowanceData](../objects-and-data-types/creditallowancedata) and [CourseAllowanceData](../objects-and-data-types/courseallowancedata).

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| ServiceKey | int | Key of the service. |
| ServiceName | string | Name of the service. |
| Credits | int (optional) | The number of credits for the service. It is present for the types `Fixed` and `Renewal`. See [CreditAllowanceType](../objects-and-data-types/creditallowancetype). |
| PublicNotes | string | Notes about the service for the patient. |
| ServiceType | [CourseServiceTypeData](../objects-and-data-types/courseservicetypedata) | Type of the service. |
| AppointmentType | [CourseAppointmentTypeData](../objects-and-data-types/courseappointmenttypedata) (optional) | The appointment type to use to book the service. It is present only in [GetPatientCourse](../courses/getpatientcourse), and only when the service can be booked online. |

## JSON Example

```json
{
    "ServiceKey": 501,
    "ServiceName": "Physiotherapy",
    "Credits": 6,
    "PublicNotes": "",
    "ServiceType": {
        "Code": "A",
        "Name": "Appointment"
    },
    "AppointmentType": {
        "Key": "PHYS",
        "Name": "Physiotherapy session"
    }
}
```
