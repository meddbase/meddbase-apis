---
layout: page
title: SaveAndSubmitQuestionnaire
nav_order: 7
parent: Questionnaire Request
---

# SaveAndSubmitQuestionnaire

Combination of [SaveQuestionnaire](../questionnaire-request/savequestionnaire) and [SubmitQuestionnaire](../questionnaire-request/submitquestionnaire). This method can be used on the latest questionnaire page where you may save the answers on the latest page and submit the questionnaire at once.

## JavaScript library method

```javascript
patientportal.questionnaireRequest.saveAndSubmitQuestionnaire({
    key: <key>,
    answers: <answers>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/questionnaire-request/save-submit-questionnaire` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| key |     | string | The validation key provided in the URL. |
| answers | [QuestionnaireAnswerData](../objects-and-data-types/questionnaireanswerdata)[] | Collection of answers. |

## Remarks

The client calls this method when all required questions are answered. After submitting the questionnaire the status will change to Complete.

When any required question is not answered the exception with event code 40001 is thrown (see [Error handling](../error-handling/error-handling)).
