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

```
patientportal.patientReportReview.getMedicalReportData({

key: &lt;key&gt;

});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/patient-report-review/review-data

## URL Parameters

| key | string | The validation key provided in the URL. |
| --- | --- | --- |

## Returns

PatientReportReviewData

## Remarks

If something goes wrong please check exception (see Error handling).
