---
layout: page
title: FollowUp
nav_order: 5
parent: Case Management
---

# FollowUp

Works the same way as the eponymously named endpoint on the referral API. Returns the case.

## JavaScript library method

```
patientportal.cases.followUp({

case: &lt;case&gt;,

reason: &lt;reason&gt;

});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/cases/follow-up

## URL Parameters

| case | string | The key of the case. |
| --- | --- | --- |

## POST Parameters

| reason | string | The reason why the user sends the follow up referral. |
| --- | --- | --- |

## Returned JSON

[CaseData](#_CaseData)
