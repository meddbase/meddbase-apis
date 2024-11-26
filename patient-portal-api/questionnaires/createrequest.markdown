---
layout: page
title: CreateRequest
nav_order: 7
parent: Questionnaires
---

# CreateRequest

Create a new questionnaire request. Either a module or a list of ad-hoc questionnaire forms can be requested. One or the other must be specified. Returns the key of the request, the same keys that are returned by [GetQuestionnaires](#_GetQuestionnaires).

## JavaScript library method

```
patientportal.questionnaires. createRequest ({

patient: &lt;patient&gt;,

moduleKey: &lt;module-key&gt;,

formKeys: &lt;form-keys&gt;

});
```

## HTTP Method

POST

## ****Url****

/patientportalapi/questionnaires/create-request

## URL Parameters

| patient | string (optional) | The key of the patient provided by the API upon GetPatients. |
| --- | --- | --- |
| module-key | string (optional) | The key of the module provided by the API upon [GetModules](#_GetModules) or a previous call to SaveModule. If not specified, a new module will be created. |

## POST Parameters

| form-keys | string\[\] (optional) | List of form keys returned from [GetQuestionnaireForms](#_GetQuestionnaireForms). |
| --- | --- | --- |

## Returned JSON

```
“ae71266c1548673052d1240115466e63a8ece5c5d3cf06abe1d006f7d975ff76”
```
