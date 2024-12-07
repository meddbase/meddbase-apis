---
layout: page
title: SubmitValidationCode
nav_order: 2
parent: Absence questionnaire
---

# SubmitValidationCode

Validates the patient using the code sent to them via a SMS message received because of a request sent to the [SendValidationSMS](../absence-questionnaire/sendvalidationsms) method.

## JavaScript library method

```javascript
patientportal.rtwQuestionnaire.submitValidationCode({
    key: <key>.
    code: <code>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/rtw-questionnaire/submit-validation-code` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| key | string | The absence key. |
| code | string | The code sent to the patient via a SMS message received because of a request sent to the [SendValidationSMS](../absence-questionnaire/sendvalidationsms) method. |

## Returns

[AbsenceRTWQuestionnaireData](../objects-and-data-types/absencertwquestionnairedata)

## Returned JSON

```json
{
    "status": "ok",
    "result": {
        "Key": "fc89c03626ab7f45ed3cf410ef1318b0",
        "StartDate": "2018-11-16T00:00:00",
        "EstimatedEndDate": "2018-11-19T00:00:00",
        "EndDate": "2018-11-26T00:00:00",
        "LostWork": {
            "Hours": 32,
            "Days": 4
        },
        "AccidentAtWork": true,
        "IsClosed": false
    }
}
```
