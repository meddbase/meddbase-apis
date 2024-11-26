---
layout: page
title: SaveQuestionnaire
nav_order: 16
parent: Appointments
---

# SaveQuestionnaire

Saves partial answers of specific questions in the questionnaire.

## JavaScript library method

```javascript
patientportal.appointment.saveQuestionnaire({
    questionnaire: <questionnaire>,
    answers: <answers>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/appointment/save-questionnaire` |

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| questionnaire | string | The key of the questionnaire provided by the API upon GetQuestionnaires. |
| answers | QuestionnaireAnswerData\[\] | Collection of answers. |

## Remarks

The client can call this method as many time as it needs. Only answers attached in parameter Answers will be updated. The sort-order of questions isn’t important.

After the first call of this method the questionnaire’s status changes to Partially Complete.

The client must call SubmitQuestionnaire after all required questions are answered.
