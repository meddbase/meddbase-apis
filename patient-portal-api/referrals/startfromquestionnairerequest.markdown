---
layout: page
title: StartFromQuestionnaireRequest
nav_order: 4
parent: Referrals
---

# StartFromQuestionnaireRequest

Starts and returns a new referral using the patient associated with the specified questionnaire request. A default appointment type is used, and the questionnaire results documents are attached to the referral. Only ‘complete’ questionnaires can be referred.

## JavaScript library method

```javascript
patientportal.referrals.startFromQuestionnaireRequest({
    questionnaireRequest: <questionnaire-request>
});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/referrals/start-from-questionnaire-request

## URL Parameters

| questionnaire-request | string | The key of the questionnaire request returned by [CreateRequest](#_CreateRequest) or [GetQuestionnaires](#_GetQuestionnaires) |
| --- | --- | --- |

## Returns

ReferralData
