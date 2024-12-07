---
layout: page
title: CreateRequest
nav_order: 7
parent: Questionnaires
---

# CreateRequest

Create a new questionnaire request. Either a module or a list of ad-hoc questionnaire forms can be requested. One or the other must be specified. Returns the key of the request, the same keys that are returned by [GetQuestionnaires](../questionnaires/getquestionnaires).

## JavaScript library method

```javascript
patientportal.questionnaires.createRequest({
    patient: <patient>,
    moduleKey: <module-key>,
    formKeys: <form-keys>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/questionnaires/create-request` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| patient | string (optional) | The key of the patient provided by the API upon [GetPatients](../patients/getpatients). |
| module-key | string (optional) | The key of the module provided by the API upon [GetModules](../questionnaires/getmodules) or a previous call to [SaveModule](../questionnaires/savemodule). If not specified, a new module will be created. |

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| form-keys | string[] (optional) | List of form keys returned from [GetQuestionnaireForms](../questionnaires/getquestionnaireforms). |

## Returned JSON

```
“ae71266c1548673052d1240115466e63a8ece5c5d3cf06abe1d006f7d975ff76”
```
