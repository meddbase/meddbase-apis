---
layout: page
title: QuestionnaireModuleData
nav_order: 70
parent: Objects and data types
---

# QuestionnaireModuleData

Provides information about a questionnaire module.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Key | string | The key of the questionnaire module. |
| Category | string | Always ‘ppq’. |
| Name | string | Name. |
| FormKeys | string[] | The keys of questionnaire forms included in the module. |

## JSON Example

```json
{
    "Key": "3bdd966cf6f9c0c6872ee0551da74c4d",
    "Category": "ppq",
    "Name": "Test",
    "FormKeys": [
        "4bdd966cf6f9c0c6872ee0551da74c4e"
    ]
}
```
