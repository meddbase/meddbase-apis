---
layout: page
title: SendValidationSMS
nav_order: 1
parent: Manager Medical Report Review
---

# SendValidationSMS

Sends the validation code through the text message.

## JavaScript library method

```javascript
patientportal.managerReportReview.sendValidationSMS({
    key: <key>
});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/manager-report-review/send-validation-sms

## URL Parameters

| key | string | The validation key provided in the URL. |
| --- | --- | --- |

## Remarks

Method does not return any data. If something goes wrong please check exception (see Error handling).
