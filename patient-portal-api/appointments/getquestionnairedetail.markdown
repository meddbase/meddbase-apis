---
layout: page
title: GetQuestionnaireDetail
nav_order: 15
parent: Appointments
---

# GetQuestionnaireDetail

Gets detail of the specific questionnaire (definitions of questions and saved patient’s answers).

## JavaScript library method

```
patientportal.appointment.getQuestionnaireDetail({questionnaire: &lt;questionnaire&gt;});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/appointment/questionnaire-detail

## URL Parameters

| questionnaire | string | The key of the questionnaire provided by the API upon GetQuestionnaires. |
| --- | --- | --- |

## Returns

QuestionnaireData
