---
layout: page
title: SaveQuestionnaire
nav_order: 5
parent: Questionnaire Request
---

# SaveQuestionnaire

Saves partial answers of specific questions in the questionnaire.

## JavaScript library method

```
patientportal.questionnaireRequest.saveQuestionnaire({

key: &lt;key&gt;,

answers: &lt;answers&gt;

});
```

## HTTP Method

POST

## ****Url****

/patientportalapi/questionnaire-request/save-questionnaire

## POST Parameters

| key | string | The validation key provided in the URL. |
| --- | --- | --- |
| answers | QuestionnaireAnswerData\[\] | Collection of answers. |

## Remarks

The client can call this method as many time as it needs. Only answers attached in parameter Answers will be updated. The sort-order of questions isn’t important.

After the first call of this method the questionnaire’s status changes to Partially Complete.

The client must call [SubmitQuestionnaire](#_SubmitQuestionnaire) after all required questions are answered.
