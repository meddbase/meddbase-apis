---
layout: page
title: FollowUp
nav_order: 5
parent: Case Management
---

# FollowUp

Works the same way as the eponymously named endpoint on the referral API. Returns the case.

## JavaScript library method

```javascript
patientportal.cases.followUp({
    case: <case>,
    reason: <reason>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/cases/follow-up` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| case | string | The key of the case. |

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| reason | string | The reason why the user sends the follow up referral. |

## Returned JSON

[CaseData](#_CaseData)
