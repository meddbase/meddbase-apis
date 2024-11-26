---
layout: page
title: GetCase
nav_order: 2
parent: Case Management
---

# GetCase

Returns a case.

## JavaScript library method

```javascript
patientportal.cases.getCase({
    case: <case>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/cases/case` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| case | string | The key of the case. |

## Returned JSON

[CaseData](#_CaseData)
