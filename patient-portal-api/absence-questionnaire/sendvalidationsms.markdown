---
layout: page
title: SendValidationSMS
nav_order: 1
parent: Absence questionnaire
---

# SendValidationSMS

Sends a validation code to the mobile phone number of the patient who is the focus of the absence record specified by the absence key.

## JavaScript library method

```javascript
patientportal.rtwQuestionnaire.sendValidationSMS({
    key: <key>
});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/rtw-questionnaire/send-validation-sms

## URL Parameters

| key | string | The absence key. |
| --- | --- | --- |

## Returned JSON

```
{

"status": "ok",

"result": “”

}
```
