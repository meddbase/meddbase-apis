---
layout: page
title: GetMedicalReportData
nav_order: 5
parent: Manager Medical Report Review
---

# GetMedicalReportData

Returns the medical report data.

The method is only valid if the current temporary security context is valid (see [SubmitValidationCode](../manager-medical-report-review/submitvalidationcode)).

## JavaScript library method

```javascript
patientportal.managerReportReview.getMedicalReportData({
    key: <key>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/manager-report-review/review-data` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| key | string | The validation key provided in the URL. |

## Returns

[ManagerReportReviewData](../objects-and-data-types/managerreportreviewdata)

## Remarks

If something goes wrong please check exception (see [Error handling](../error-handling/error-handling)).
