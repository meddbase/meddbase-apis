---
layout: page
title: ValidateKey
nav_order: 3
parent: Absence questionnaire
---

# ValidateKey

Checks whether the code sent to the patient because of a request to the [SendValidationSMS](../absence-questionnaire/sendvalidationsms) method is still valid.

## JavaScript library method

```javascript
patientportal.rtwQuestionnaire.validateKey({
    key: <key>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/rtw-questionnaire/validate-key` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| key | string | The absence key. |

## Returned JSON

```json
{
    "status": "ok",
    "result": “”
}
```

or:

```json
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
