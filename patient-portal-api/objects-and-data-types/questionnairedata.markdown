---
layout: page
title: QuestionnaireData
nav_order: 68
parent: Objects and data types
---

# QuestionnaireData

Contains the information about the questionnaire including questions and answers.

## Properties

<table><tbody><tr><th><p>Key</p></th><th><p>string</p></th><th><p>Key of the questionnaire.</p></th></tr><tr><td><p>Name</p></td><td><p>string</p></td><td><p>Name of the questionnaire.</p></td></tr><tr><td><p>Description</p></td><td><p>string</p></td><td><p>Description of the questionnaire.</p></td></tr><tr><td><p>StatusCode</p></td><td><p>int</p></td><td><p>Status code of the questionnaire:</p><ul><li>0 = Incomplete</li><li>1 = Complete</li><li>2 = Partially Complete</li></ul></td></tr><tr><td><p>Status</p></td><td><p>string</p></td><td><p>String representation of the status code.</p></td></tr><tr><td><p>AppointmentKey</p></td><td><p>string</p></td><td><p>The appointment the questionnaire is created for.</p></td></tr><tr><td><p>Expiration</p></td><td><p>DateTime</p></td><td><p>When the questionnaire expires.</p></td></tr><tr><td><p>Answers</p></td><td><p>QuestionnaireAnswerData[]</p></td><td><p>All saved answers for this questionnaire.</p></td></tr><tr><td><p>Markup</p></td><td><p>string</p></td><td><p>XML contains questions. See Questionnaire markup.</p></td></tr></tbody></table>

## JSON Example

```
{

"Key": "q13788",

"Name": "Basic questionnaire",

"Description": "",

"StatusCode": 0,

"Status": "Incomplete",

"AppointmentKey": "apt5821",

"Expiration": "2013-08-25",

"Answers": \[

{

"QuestionId": 236,

"Answer": "Yes"

},

{

"QuestionId": 237,

"Answer": "No"

}

\],

Markup = "&lt;?xml version=\\"1.0\\" encoding=\\"utf-8\\"?&gt;&lt;Questionnaire&gt; see Questionnaire markup to see full markup"

}
```
