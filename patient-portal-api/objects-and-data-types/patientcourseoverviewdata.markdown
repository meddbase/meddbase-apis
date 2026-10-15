---
layout: page
title: PatientCourseOverviewData
nav_order: 101
parent: Objects and data types
---

# PatientCourseOverviewData

A course that a patient has bought, without the credit balances.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Key | string | Key of the patient course. Use it in the `patient-course` parameter of [GetPatientCourse](../courses/getpatientcourse) and of the appointment methods. |
| CourseKey | string | Key of the course that was bought. Use it in the `course` parameter of [GetCourse](../courses/getcourse). |
| Code | string | Code of the course. |
| Name | string | Name of the course. |
| PublicNotes | string | Notes about the course for the patient. |
| FirstIncludedDay | string | The first day of the patient course, in the format `yyyy-MM-dd`. |
| LastIncludedDay | string | The last day of the patient course, in the format `yyyy-MM-dd`. |
| Status | [PatientCourseState](../objects-and-data-types/patientcoursestate) | The status of the patient course. |

## JSON Example

```json
{
    "Key": "8ebb55f10382d73e494e7207d1bd7272",
    "CourseKey": "c31a0f7e2b94d5581e6f70a3b2c49d10",
    "Code": "EHP",
    "Name": "Executive Health Programme",
    "PublicNotes": "Annual health programme.",
    "FirstIncludedDay": "2026-07-01",
    "LastIncludedDay": "2027-06-30",
    "Status": "Active"
}
```
