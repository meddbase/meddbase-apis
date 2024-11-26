---
layout: page
title: GetQuestionnaireResults
nav_order: 4
parent: Questionnaires
---

# GetQuestionnaireResults

Get the results of a questionnaire request. The result of this call is an array of result objects, one for each questionnaire in the request. Each result has the HTML markup of a results document created from the answers.

## JavaScript library method

```javascript
patientportal.questionnaires. getQuestionnaireResults({
    questionnaireRequest: <questionnaire-request>
});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/questionnaires/results

## URL Parameters

| questionnaire-request | string | The key of the questionnaire request returned by [CreateRequest](#_CreateRequest) or [GetQuestionnaires](#_GetQuestionnaires) |
| --- | --- | --- |

## Returns

[QuestionnaireResultData](#_QuestionnaireResultData)\[\]
