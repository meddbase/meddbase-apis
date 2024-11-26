---
layout: page
title: SubmitValidationCode
nav_order: 2
parent: Absence questionnaire
---

# SubmitValidationCode

Validates the patient using the code sent to them via a SMS message received because of a request sent to the [SendValidationSMS](#_SendValidationSMS) method.

## JavaScript library method

```javascript
patientportal.rtwQuestionnaire.submitValidationCode ({
    key: <key>.
    code: <code>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/rtw-questionnaire/submit-validation-code` |

## URL Parameters

| key | string | The absence key. |
| --- | --- | --- |
| code | string | The code sent to the patient via a SMS message received because of a request sent to the [SendValidationSMS](#_SendValidationSMS) method. |

## Returned JSON

```
{

"status": "ok",

"result": {

<[AbsenceRTWQuestionnaireData](#_AbsenceRTWQuestionnaireData)\>

}

}
```
