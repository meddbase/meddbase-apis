---
layout: page
title: AbsenceRTWQuestionnaireData
nav_order: 3
parent: Objects and data types
---

# AbsenceRTWQuestionnaireData

The data returned in the response of a call to the [SubmitValidationCode](#_SubmitValidationCode) method, to be modified if necessary and posted back to the API in a request to the [SubmitQuestionnaire](#_SubmitQuestionnaire_1) method.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Key | int | The key of the absence record. |
| StartDate | [DateTime](../objects-and-data-types/datetime) (read-only) | The date that the absence started. |
| EstimatedEndDate | [DateTime](../objects-and-data-types/datetime) (read-only) | The estimated return-to-work date. |
| EndDate | [DateTime](../objects-and-data-types/datetime) (optional) | The actual return-to-work date. |
| LostWork | [LostWork](../objects-and-data-types/lostwork) | The details about the amount of work lost due to the absence. |
| AccidentAtWork | bool | Whether the absence was caused by an accident at work. |
| IsClosed | bool | Whether the absence has been closed. |

## JSON Example

```
{

"status": "ok",

"result": {

"Key": "fc89c03626ab7f45ed3cf410ef1318b0",

"StartDate": "2018-11-16T00:00:00",

"EstimatedEndDate": "2018-11-19T00:00:00",

"EndDate": "2018-11-26T00:00:00",

"LostWork": {

<[LostWork](../objects-and-data-types/lostwork)\>

},

"AccidentAtWork": true,

"IsClosed": false

}

}
```
