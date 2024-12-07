---
layout: page
title: SaveAndSubmitQuestionnaire
nav_order: 18
parent: Appointments
---

# SaveAndSubmitQuestionnaire

Combination of [SaveQuestionnaire](../appointments/savequestionnaire) and [SubmitQuestionnaire](../appointments/submitquestionnaire). This method can be used on the latest questionnaire page where you may save the answers on the latest page and submit the questionnaire at once.

## JavaScript library method

```javascript
patientportal.appointment.saveAndSubmitQuestionnaire({
    questionnaire: <questionnaire>,
    answers: <answers>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/appointment/save-submit-questionnaire` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| questionnaire | string | The key of the questionnaire provided by the API upon [GetQuestionnaires](../appointments/getquestionnaires). |
| answers | [QuestionnaireAnswerData](../objects-and-data-types/questionnaireanswerdata)[] | Collection of answers. |

## Remarks

The client calls this method when all required questions are answered. After submitting the questionnaire the status will change to Complete. The questionnaire is still accessible using [GetQuestionnaires](../appointments/getquestionnaires) until the appointment starts (in real-life).

When any required question is not answered the exception with event code 40001 is thrown (see [Error handling](../error-handling/error-handling)).
