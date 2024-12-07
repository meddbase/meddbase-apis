---
layout: page
title: SendValidationSMS
nav_order: 1
parent: Patient Medical Report Review
---

# SendValidationSMS

Sends the validation code through the text message.

## JavaScript library method

```javascript
patientportal.patientReportReview.sendValidationSMS({
    key: <key>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/patient-report-review/send-validation-sms` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| key | string | The validation key provided in the URL. |

## Remarks

Method does not return any data. If something goes wrong please check exception (see [Error handling](../error-handling/error-handling)).
