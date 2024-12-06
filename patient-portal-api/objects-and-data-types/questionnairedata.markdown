---
layout: page
title: QuestionnaireData
nav_order: 68
parent: Objects and data types
---

# QuestionnaireData

Contains the information about the questionnaire including questions and answers.

## Properties

<table>
    <thead>
        <tr>
            <th style="text-align: left">Parameter</th>
            <th style="text-align: left">Type</th>
            <th style="text-align: left">Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Key</td>
            <td>string</td>
            <td>Key of the questionnaire.</td>
        </tr>
        <tr>
            <td>Name</td>
            <td>string</td>
            <td>Name of the questionnaire.</td>
        </tr>
        <tr>
            <td>Description</td>
            <td>string</td>
            <td>Description of the questionnaire.</td>
        </tr>
        <tr>
            <td>StatusCode</td>
            <td>int</td>
            <td>
                <p>Status code of the questionnaire:</p>
                <ul>
                    <li>0 = Incomplete</li>
                    <li>1 = Complete</li>
                    <li>2 = Partially Complete</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Status</td>
            <td>string</td>
            <td>String representation of the status code.</td>
        </tr>
        <tr>
            <td>AppointmentKey</td>
            <td>string</td>
            <td>The appointment the questionnaire is created for.</td>
        </tr>
        <tr>
            <td>Expiration</td>
            <td><a href="../objects-and-data-types/datetime">DateTime</a></td>
            <td>When the questionnaire expires.</td>
        </tr>
        <tr>
            <td>Answers</td>
            <td><a href="../objects-and-data-types/questionnaireanswerdata">QuestionnaireAnswerData</a>[]</td>
            <td>All saved answers for this questionnaire.</td>
        </tr>
        <tr>
            <td>Markup</td>
            <td>string</td>
            <td>XML contains questions. See Questionnaire markup.</td>
        </tr>
    </tbody>
</table>

## JSON Example

```json
{
    "Key": "q13788",
    "Name": "Basic questionnaire",
    "Description": "",
    "StatusCode": 0,
    "Status": "Incomplete",
    "AppointmentKey": "apt5821",
    "Expiration": "2013-08-25",
    "Answers": [
        {
            "QuestionId": 236,
            "Answer": "Yes"
        },
        {
            "QuestionId": 237,
            "Answer": "No"
        }
    ],
    "Markup": "<?xml version=\"1.0\" encoding=\"utf-8\"?><Questionnaire> see Questionnaire markup to see full markup"
}
```
