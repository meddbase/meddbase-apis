---
layout: page
title: OpenCase
nav_order: 3
parent: Case Management
---

# OpenCase

Opens a case and returns the newly opened case.

## JavaScript library method

```javascript
patientportal.cases.openCase({
    case: <case>
});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/cases/open-case

## URL Parameters

| case | string | The key of the case. |
| --- | --- | --- |

## Returned JSON

[CaseData](#_CaseData)
