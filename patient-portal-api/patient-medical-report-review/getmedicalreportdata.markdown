---
layout: page
title: GetMedicalReportData
nav_order: 5
parent: Patient Medical Report Review
---

# GetMedicalReportData

Returns the medical report data.

The method is only valid if the current temporary security context is valid (see SubmitValidationCode).

## JavaScript library method

```javascript
patientportal.patientReportReview.getMedicalReportData({
    key: <key>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/patient-report-review/review-data` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| key | string | The validation key provided in the URL. |

## Returns

PatientReportReviewData

## Remarks

If something goes wrong please check exception (see Error handling).
