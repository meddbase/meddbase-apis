---
layout: page
title: QuestionnaireResultData
nav_order: 72
parent: Objects and data types
---

# QuestionnaireResultData

Provides the results of a questionnaire request.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Complete | bool | True if the patient has finally submitted the results. |
| Name | string | Name of the questionnaire. |
| Html | string | The Html markup of the results document which contains the formatted results. |

## JSON Example

```json
{
    "Complete": true,
    "Name": "Test",
    "Html": "…"
}
```
