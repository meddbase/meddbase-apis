---
layout: page
title: GetCourse
nav_order: 2
parent: Courses
---

# GetCourse

Returns one course as the chamber sells it, with its credit allowances.

## JavaScript library method

```javascript
patientportal.courses.getCourse({
    course: <course>,
    payerType: <payer-type>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/courses/course` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| course | string | The key of the course provided by the API upon [GetCourses](../courses/getcourses). |
| payer-type | string | The payer type that provides the price.<br><br>When the client is logged in, use the key of a payer type from the result of [GetCourses](../courses/getcourses). When the client is not logged in, use a charge-band sign-up code. |

## Returns

[CourseData](../objects-and-data-types/coursedata)

## Remarks

This method can be used without login. See [Courses](../courses/courses).

An error is returned if:

- the payer type is not valid for the patient (logged in), or is not a valid sign-up code (not logged in);
- the key is not the key of a course;
- the course is not available to buy for the payer type.

The credit allowances come from the credit rules of the course. A rule is not in the result if it gives no services, has no valid dates or has already ended. A service that is withdrawn is not in the result. The services are sorted by name.

The result is not for a patient, so it has no balances.
