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

<table><tbody><tr><th><p>Key</p></th><th><p>string</p></th><th><p>Key of the questionnaire.</p></th></tr><tr><td><p>Name</p></td><td><p>string</p></td><td><p>Name of the questionnaire.</p></td></tr><tr><td><p>Description</p></td><td><p>string</p></td><td><p>Description of the questionnaire.</p></td></tr><tr><td><p>StatusCode</p></td><td><p>int</p></td><td><p>Status code of the questionnaire:</p><ul><li>0 = Incomplete</li><li>1 = Complete</li><li>2 = Partially Complete</li></ul></td></tr><tr><td><p>Status</p></td><td><p>string</p></td><td><p>String representation of the status code.</p></td></tr><tr><td><p>AppointmentKey</p></td><td><p>string</p></td><td><p>The appointment the questionnaire is for.</p></td></tr><tr><td><p>Expiration</p></td><td><p>DateTime</p></td><td><p>When the questionnaire expires.</p></td></tr><tr><td><p>Sent</p></td><td><p>DateTime (optional)</p></td><td><p>When the questionnaire was sent.</p></td></tr><tr><td><p>ReferralKey</p></td><td><p>string (optional)</p></td><td><p>If present, the key of a referral that was created from the questionnaire request.</p></td></tr><tr><td><p>CanRefer</p></td><td><p>bool (optional)</p></td><td><p>Whether the questionnaire indicates a referral.</p></td></tr></tbody></table>

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
