---
layout: page
title: SubmitAuthorisation
nav_order: 6
parent: Patient Medical Report Review
---

# SubmitAuthorisation

Release or refuse the medical report and stores patient’s comments and requested factual changes.

The method is only valid if the current temporary security context is valid (see [SubmitValidationCode](../patient-medical-report-review/submitvalidationcode)).

## JavaScript library method

```javascript
patientportal.patientReportReview.submitAuthorisation({
    key: <key>,
    authorised: <authorised>,
    comments: <comments>,
    factualChanges: [
        {
            Subject: <Subject>,
            Comments: <Comments>
        }
    ]
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
| authorised | bool | true if the patient releases the medical report, false if the patient refuses it. |

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| comments | string | Comments provided by the patient. |
| factualChanges | \[<br><br>{<br><br>Subject: string,<br><br>Comments: string<br><br>} ,…<br><br>\] | List of factual changes requested by the patient.<br><br>Subject – Subject of possible factual changes provided by the API (see [PatientReportReviewData](../objects-and-data-types/patientreportreviewdata))<br><br>Comments – Patient’s comments |

## Returns

[PatientReportReviewData](../objects-and-data-types/patientreportreviewdata)

## Remarks

Calling this method removes the security context so no other command ([GetMedicalReportData](../patient-medical-report-review/getmedicalreportdata), [SubmitAuthorisation](../patient-medical-report-review/submitauthorisation)) is allowed without new validation. If something goes wrong please check exception (see [Error handling](../error-handling/error-handling)).
