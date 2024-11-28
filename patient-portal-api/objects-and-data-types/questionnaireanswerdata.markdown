---
layout: page
title: QuestionnaireAnswerData
nav_order: 67
parent: Objects and data types
---

# QuestionnaireAnswerData

Answer for the questionnaire question.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| QuestionId | long | Id of the question from the questionnaire markup. |
| Answer | string | Answer of the question. |
| Answers | string[] | Answers of the question. Used if the answer includes more answers. |

## JSON Example

```json
{
    "QuestionId": 236,
    "Answer": "Yes",
    "Answers": [
        "Yes"
    ]
}
```
