---
layout: page
title: GetModules
nav_order: 2
parent: Questionnaires
---

# GetModules

Returns the list of questionnaire modules that are visible for the logged in user. Modules are visible if they are created by the user or shared by another user.

## JavaScript library method

```javascript
patientportal.questionnaires. getModules({
    category: ’ppq’,
    moduleName: <module-name>,
    pageNumber: <page-number>,
    pageSize: <page-size>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/questionnaires/modules` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| category | string (required) | Always ‘ppq’. |
| module-name | string (optional) | Filter for module name. |
| page-number | int (optional) | Page number. Default 1. |
| page-size | int (optional) | Page size. Default 10. Minimum 5. Maximum 50. |

## Returns

[QuestionnaireModuleData](../objects-and-data-types/questionnairemoduledata)[]

## Returned JSON

```json
{
    "Items": [
        {
            "Key": "3bdd966cf6f9c0c6872ee0551da74c4d",
            "Category": "ppq",
            "Name": "Test",
            "FormKeys": [
                "4bdd966cf6f9c0c6872ee0551da74c4e"
            ]
        }
    ],
    "TotalCount":1,
    "CurrentPage":1,
    "PageSize":10
}
```
