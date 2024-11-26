---
layout: page
title: SendValidationSMS
nav_order: 1
parent: Absence questionnaire
---

# SendValidationSMS

Sends a validation code to the mobile phone number of the patient who is the focus of the absence record specified by the absence key.

## JavaScript library method

```
patientportal.rtwQuestionnaire.sendValidationSMS ({

key: &lt;key&gt;

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
