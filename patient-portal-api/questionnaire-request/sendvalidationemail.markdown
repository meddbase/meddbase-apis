---
layout: page
title: SendValidationEmail
nav_order: 2
parent: Questionnaire Request
---

# SendValidationEmail

Sends the validation code through the email.

## JavaScript library method

```javascript
patientportal.questionnaireRequest.sendValidationEmail({
    key: <key>
});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/questionnaire-request/send-validation-email

## URL Parameters

| key | string | The validation key provided in the URL. |
| --- | --- | --- |

## Remarks

Method does not return any data. If something goes wrong please check exception (see Error handling).
