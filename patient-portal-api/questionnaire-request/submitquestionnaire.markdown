---
layout: page
title: SubmitQuestionnaire
nav_order: 6
parent: Questionnaire Request
---

# SubmitQuestionnaire

Submits the specific questionnaire.

## JavaScript library method

```javascript
patientportal.questionnaireRequest.submitQuestionnaire({key: <key>});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/questionnaire-request/submit-questionnaire

## URL Parameters

| key | string | The validation key provided in the URL. |
| --- | --- | --- |

## Remarks

The client calls this method when all required questions are answered. After submitting the questionnaire the status will change to Complete.

When any required question is not answered the exception with event code 40001 is thrown (see Error handling).
