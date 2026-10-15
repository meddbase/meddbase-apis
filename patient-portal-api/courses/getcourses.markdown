---
layout: page
title: GetCourses
nav_order: 1
parent: Courses
---

# GetCourses

Returns the courses that the patient can buy online, grouped by payer type.

## JavaScript library method

```javascript
patientportal.courses.getCourses({
    payerType: <payer-type>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/courses/courses` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| payer-type | string (optional) | The sign-up code of a charge band, that will provide the prices.<br><br>The client must provide this parameter when it is not logged in. The server ignores it when the client is logged in. |

## Returns

[PayerCoursesData](../objects-and-data-types/payercoursesdata)[]

## Remarks

This method can be used without login. See [Courses](../courses/courses).

When the client is logged in:

- The result has one group for each payer type that the patient can use to book. A payer type that has no courses is not in the result.
- The prices are the prices of the charge band of the payer type. If a course is VAT exempt, `Tax` is 0 and `GrossPrice` is equal to `NetPrice`.

When the client is not logged in:

- The `payer-type` parameter must be a valid sign-up code. If it is missing or not valid, an error is returned.
- The result has one group. `Key` and `Name` of its [PayerType](../objects-and-data-types/payertype) are both the sign-up code.
- The prices do not depend on the patient, so the sex and the age of the patient are not used.

The result does not contain the credit allowances of the courses. Use [GetCourse](../courses/getcourse) to get them.

Use `Key` of a course in the `course` parameter of [GetCourse](../courses/getcourse) and [Purchase](../courses/purchase).
