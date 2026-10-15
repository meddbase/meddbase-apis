---
layout: page
title: GetPatientCourses
nav_order: 4
parent: Courses
---

# GetPatientCourses

Returns the courses that the logged in patient has bought.

## JavaScript library method

```javascript
patientportal.patientCourses.getPatientCourses({
    status: <status>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/patient-courses/patient-courses` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| status | string (optional) | Returns only the patient courses with this status. The value is one of `Active`, `Completed`, `Refunded` and `Expired`. The letter case does not matter. See [PatientCourseState](../objects-and-data-types/patientcoursestate).<br><br>If the parameter is not present, the method returns patient courses with all statuses. |

## Returns

[PatientCourseOverviewData](../objects-and-data-types/patientcourseoverviewdata)[]

## Remarks

The result contains the active patient courses first. Inside each group the newest `FirstIncludedDay` is first.

The result does not contain balances. Use [GetPatientCourse](../courses/getpatientcourse) to get them.

If the value of `status` is not a valid status, an error is returned.

Use `Key` of a patient course in the `patient-course` parameter of [GetPatientCourse](../courses/getpatientcourse) and of the appointment methods. `CourseKey` is the key of the course that was bought. It can be used in the `course` parameter of [GetCourse](../courses/getcourse).
