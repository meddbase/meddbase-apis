---
layout: page
title: SubmitQuestionnaire
nav_order: 4
parent: Absence questionnaire
---

# SubmitQuestionnaire

Checks whether the code sent to the patient because of a request to the [SendValidationSMS](#_SendValidationSMS_1) method is still valid.

## JavaScript library method

```
patientportal.rtwQuestionnaire.submitQuestionnaire ({

rtwQuestionnaireData: &lt;rtw-questionnaire-data&gt;

});
```

## HTTP Method

POST

## ****Url****

/patientportalapi/rtw-questionnaire/submit-questionnaire

## URL Parameters

| rtw-questionnaire-data | [AbsenceRTWQuestionnaireData](#_AbsenceRTWQuestionnaireData) | An [AbsenceRTWQuestionnaireData](#_AbsenceRTWQuestionnaireData) object, as received from the [SubmitValidationCode](#_SubmitValidationCode) method. |
| --- | --- | --- |

## Returned JSON

```
{

"status": "ok",

"result": “”

}
```
