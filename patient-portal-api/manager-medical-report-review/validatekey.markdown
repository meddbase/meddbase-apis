---
layout: page
title: ValidateKey
nav_order: 4
parent: Manager Medical Report Review
---

# ValidateKey

Validates whether the security context for the last submitted validation code is still valid.

## JavaScript library method

```javascript
patientportal.managerReportReview.validateKey({
    key: <key>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/manager-report-review/validate-key` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| key | string | The validation key provided in the URL. |

## Remarks

Method does not return any data. If something goes wrong please check exception (see [Error handling](../error-handling/error-handling)).

If the security context runs out the manager may request another validation code and submit it to create new security context.
