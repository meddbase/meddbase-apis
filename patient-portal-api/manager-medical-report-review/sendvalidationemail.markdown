---
layout: page
title: SendValidationEmail
nav_order: 2
parent: Manager Medical Report Review
---

# SendValidationEmail

Sends the validation code through the email.

## JavaScript library method

```javascript
patientportal.managerReportReview.sendValidationEmail({
    key: <key>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/manager-report-review/send-validation-email` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| key | string | The validation key provided in the URL. |

## Remarks

Method does not return any data. If something goes wrong please check exception (see [Error handling](../error-handling/error-handling)).
