---
layout: page
title: SubmitQuestionnaire
nav_order: 17
parent: Appointments
---

# SubmitQuestionnaire

Submits the specific questionnaire.

## JavaScript library method

```javascript
patientportal.appointment.submitQuestionnaire({questionnaire: <questionnaire>});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/appointment/submit-questionnaire

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| questionnaire | string | The key of the questionnaire provided by the API upon GetQuestionnaires. |

## Remarks

The client calls this method when all required questions are answered. After submitting the questionnaire the status will change to Complete. The questionnaire is still accessible using GetQuestionnaires until the appointment starts (in real-life).

When any required question is not answered the exception with event code 40001 is thrown (see Error handling).
