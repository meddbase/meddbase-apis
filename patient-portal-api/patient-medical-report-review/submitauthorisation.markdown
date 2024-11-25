---
layout: page
title: SubmitAuthorisation
nav_order: 6
parent: Patient Medical Report Review
---

# SubmitAuthorisation

Release or refuse the medical report and stores patient’s comments and requested factual changes.

The method is only valid if the current temporary security context is valid (see SubmitValidationCode).

## JavaScript library method

```javascript
patientportal.patientReportReview.submitAuthorisation({
    key: <key>,
    authorised: <authorised>,
    comments: <comments>,
    factualChanges:\[
    {
    Subject: <Subject>,
    Comments: <Comments>
},
    ...
    \]
});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/patient-report-review/review-data

## URL Parameters

| key | string | The validation key provided in the URL. |
| --- | --- | --- |
| authorised | bool | true if the patient releases the medical report, false if the patient refuses it. |

## POST Parameters

| comments | string | Comments provided by the patient. |
| --- | --- | --- |
| factualChanges | \[<br><br>{<br><br>Subject: string,<br><br>Comments: string<br><br>} ,…<br><br>\] | List of factual changes requested by the patient.<br><br>Subject – Subject of possible factual changes provided by the API (see PatientReportReviewData)<br><br>Comments – Patient’s comments |

## Returns

PatientReportReviewData

## Remarks

Calling this method removes the security context so no another command (GetMedicalReportData, SubmitAuthorisation) is allowed without new validation. If something goes wrong please check exception (see Error handling).
