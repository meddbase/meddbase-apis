---
layout: page
title: QuestionnaireOverviewData
nav_order: 71
parent: Objects and data types
---

# QuestionnaireOverviewData

The questionnaire overview contains basic information about the questionnaire.

Overview data doesn’t contains questions and answers.

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
            <td>The appointment the questionnaire is for.</td>
        </tr>
        <tr>
            <td>Expiration</td>
            <td><a href="../objects-and-data-types/datetime">DateTime</a></td>
            <td>When the questionnaire expires.</td>
        </tr>
        <tr>
            <td>Sent</td>
            <td><a href="../objects-and-data-types/datetime">DateTime</a> (optional)</td>
            <td>When the questionnaire was sent.</td>
        </tr>
        <tr>
            <td>ReferralKey</td>
            <td>string (optional)</td>
            <td>If present, the key of a referral that was created from the questionnaire request.</td>
        </tr>
        <tr>
            <td>CanRefer</td>
            <td>bool (optional)</td>
            <td>Whether the questionnaire indicates a referral.</td>
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
    "Sent": "2013-07-01",
    "ReferralKey": "8ebb55f10382d73e494e7207d1bd7272",
    "CanRefer": 0
}
```
