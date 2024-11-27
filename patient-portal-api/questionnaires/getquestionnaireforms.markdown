---
layout: page
title: GetQuestionnaireForms
nav_order: 1
parent: Questionnaires
---

# GetQuestionnaireForms

Returns the list of questionnaire forms that can be requested for any patient. If a module is specified then only the forms included in that module are returned.

## JavaScript library method

```javascript
patientportal.questionnaires. getQuestionnaireForms({
    moduleKey: <module-key>,
    category: ’ppq’,
    formName: <form-name>,
    pageNumber: <page-number>,
    pageSize: <page-size>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/questionnaires/forms` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| module-key | string (optional) | The key of the module provided by the API upon GetModules. |
| category | string (required) | Always ‘ppq’. |
| form-name | string (optional) | Filter for form name. |
| page-number | int (optional) | Page number. Default 1. |
| page-size | int (optional) | Page size. Default 10. Minimum 5. Maximum 50. |

## Returns

[QuestionnaireFormData](../objects-and-data-types/questionnaireformdata)[]

## Returned JSON

```json
{
    "Items": [
        {
            "Key": "3bdd966cf6f9c0c6872ee0551da74c4d",
            "Category": "ppq",
            "Name": "Test",
            "Description": "Longer description"
        }
    ],
    "TotalCount":1,
    "CurrentPage":1,
    "PageSize":10
}
```
