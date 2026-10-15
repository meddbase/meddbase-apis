---
layout: page
title: Purchase
nav_order: 3
parent: Courses
---

# Purchase

Buys a course for the logged in patient. The method creates a patient course and raises an invoice for it.

## JavaScript library method

```javascript
patientportal.courses.purchase({
    course: <course>,
    payerType: <payer-type>,
    startDate: <start-date>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/courses/purchase` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| course | string | The key of the course provided by the API upon [GetCourses](../courses/getcourses). |
| payer-type | string | The key of the payer type provided by the API upon [GetCourses](../courses/getcourses). |
| start-date | [DateTime](../objects-and-data-types/datetime) (optional) | The first day of the patient course. Only the date is used. The date cannot be earlier than today. Default is today. |

## Returns

[PurchaseResultData](../objects-and-data-types/purchaseresultdata)

## Remarks

The method does not take a payment. To pay the invoice, use [ProvidePayment](../finance/providepayment) with the key of the invoice.

The payer type must be one that the patient can use. The course must be available to buy for the payer type. If not, an error is returned.

The invoice is raised to the account of the payer. If the payer has no account, the invoice is raised to the account of the patient.

The patient course ends after the expiry period of the course, counted from the start date.

The method does not check if the patient already has the same course. Each successful call creates a new patient course and a new invoice.

If the start date is earlier than today, or the purchase cannot be completed, an error is returned, see [Error handling](../error-handling/error-handling).

The parameters go in the URL. The JavaScript library sends an empty JSON object as the request body.
