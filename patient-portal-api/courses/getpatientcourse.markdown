---
layout: page
title: GetPatientCourse
nav_order: 5
parent: Courses
---

# GetPatientCourse

Returns one course that the logged in patient has bought, with the credit balances.

## JavaScript library method

```javascript
patientportal.patientCourses.getPatientCourse({
    patientCourse: <patient-course>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/patient-courses/patient-course` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| patient-course | string | The key of the patient course provided by the API upon [GetPatientCourses](../courses/getpatientcourses) or [Purchase](../courses/purchase). |

## Returns

[PatientCourseData](../objects-and-data-types/patientcoursedata)

## Remarks

The method finds only the patient courses of the logged in patient. If the patient course is not found, or it belongs to another patient, an error is returned.

The credit allowances are the credit rules of the course, calculated for this patient and this patient course. A rule is not in the result if it gives no services or has no valid dates. A rule with a sex restriction is not in the result if the restriction does not match the patient. A withdrawn service is not in the result.

If a rule gives credits for each service separately, the result has one allowance for each service. If a rule gives one shared pool of credits for a group of services, the result has one allowance for the group. Because of this, the number of allowances can be different from the number in [GetCourse](../courses/getcourse).

Each allowance has either `Balance` (the credits do not renew) or `Period` (the credits renew), but not both.

`CanBookOnline` is true if at least one service of the course can be booked online. It is always false if `Status` is not `Active`. When `CanBookOnline` is true, `AppointmentType` of a service is the appointment type to use to book the service. To book, send the key of the patient course in the `patient-course` parameter of the appointment methods. See [Courses](../courses/courses).
