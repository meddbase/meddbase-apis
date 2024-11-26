---
layout: page
title: ValidateKey
nav_order: 3
parent: Absence questionnaire
---

# ValidateKey

Checks whether the code sent to the patient because of a request to the [SendValidationSMS](#_SendValidationSMS_1) method is still valid.

## JavaScript library method

```javascript
patientportal.rtwQuestionnaire.validateKey({
    key: <key>
});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/rtw-questionnaire/validate-key

## URL Parameters

| key | string | The absence key. |
| --- | --- | --- |

## Returned JSON

```
{

"status": "ok",

"result": “”

}

or:

{

"status": "error",

"error": {

"Message": "Validation code has expired. Please re-send new validation code.",

"EventType": 2,

"StatusCode": 500,

"EventCode": 0

}

}
```
