---
layout: page
title: SendValidationSMS
nav_order: 1
parent: Questionnaire Request
---

# SendValidationSMS

Sends the validation code through the text message.

## JavaScript library method

```javascript
patientportal.questionnaireRequest.sendValidationSMS({
    key: <key>
});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/questionnaire-request/send-validation-sms

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| key | string | The validation key provided in the URL. |

## Remarks

Method does not return any data. If something goes wrong please check exception (see Error handling).
