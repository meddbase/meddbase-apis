---
layout: page
title: SubmitValidationCode
nav_order: 3
parent: Manager Medical Report Review
---

# SubmitValidationCode

Submits the validation code and returns the medical report review data. Once the validation code is submitted a temporary security context is created.

## JavaScript library method

```javascript
patientportal.managerReportReview.submitValidationCode({
    key: <key>,
    code: <code>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/manager-report-review/submit-validation-code` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| key | string | The validation key provided in the URL. |
| code | string | The validation code the manager gets through the email or text message. |

## Returns

[ManagerReportReviewData](../objects-and-data-types/managerreportreviewdata)

## Remarks

Submitting the validation code creates a temporary security context which is valid for 30 minutes. Within this time frame the manager needs to review the medical report and submit the authorisation.

The client may use ValidateKey to verify whether the security context runs out and request new validation code to create a new security context.

If something goes wrong please check exception (see Error handling).
