---
layout: page
title: PathwayData
nav_order: 50
parent: Objects and data types
---

# PathwayData

Provides full details about the pathway.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Key | string | The key of the pathway. |
| Number | string | The number of the pathway. |
| Name | string | The name of the pathway. |
| Patient | string | The name of the patient. |
| ReadOnly | bool | True if the pathway is currently in a read-only mode. |
| Tasks | [PathwayTaskOverviewData](../objects-and-data-types/pathwaytaskoverviewdata)[] | The list of pathways tasks. |

## JSON Example

```
{

"Key": "a1d3e2d1",

"Number": "123",

"Name": "Book & Arrive",

"Patient": "Mr. Will Smith",

"ReadOnly": false,

"Tasks": \[

{

"Name": "GT",

"ActionType": "GT",

"ActionTypeName": "General task",

"StateType": "ST",

"StateName": "Started",

"CanProcess": true,

"Key": "62cf82832e12453faf8c9813f7817f7e",

},

{

"Name": "AD",

"ActionType": "AD",

"ActionTypeName": "Attach a document",

"StateType": "FT",

"StateName": "Future task",

"CanProcess": false,

"Key": "df19272dc84b4f2c511ed2a04b616d1a",

},

{

"Name": "BA",

"ActionType": "BA",

"ActionTypeName": "Book an appointment",

"StateType": "FT",

"StateName": "Future task",

"CanProcess": false,

"Key": "0ddf1c6b831d08fe5ccdb65fd76a4665",

},

{

"Name": "AQ",

"ActionType": "QR",

"ActionTypeName": "Answer a questionnaire",

"StateType": "FT",

"StateName": "Future task",

"CanProcess": false,

"Key": "81aadeae6b9535135ed1c8dfc83a81b7",

},

{

"Name": "AA",

"ActionType": "AA",

"ActionTypeName": "Arrive an appointment",

"StateType": "FT",

"StateName": "Future task",

"CanProcess": false,

"Key": "86149d568252ae476859a3a60835369b",

}

\]

}
```
