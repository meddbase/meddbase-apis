---
layout: page
title: SubmitQuestionnaire
nav_order: 4
parent: Absence questionnaire
---

# SubmitQuestionnaire

Checks whether the code sent to the patient because of a request to the [SendValidationSMS](#_SendValidationSMS_1) method is still valid.

## JavaScript library method

```javascript
patientportal.rtwQuestionnaire.submitQuestionnaire({
    rtwQuestionnaireData: <rtw-questionnaire-data>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/rtw-questionnaire/submit-questionnaire` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| rtw-questionnaire-data | [AbsenceRTWQuestionnaireData](../objects-and-data-types/absencertwquestionnairedata) | An [AbsenceRTWQuestionnaireData](../objects-and-data-types/absencertwquestionnairedata) object, as received from the [SubmitValidationCode](#_SubmitValidationCode) method. |

## Returned JSON

```json
{
    "status": "ok",
    "result": “”
}
```
