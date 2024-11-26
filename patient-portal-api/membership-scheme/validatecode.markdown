---
layout: page
title: ValidateCode
nav_order: 1
parent: Membership scheme
---

# ValidateCode

Confirms the validity of the membership scheme code.

## JavaScript library method

```
patientportal.membershipScheme.validateCode({code: &lt;code&gt;});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/membership-scheme/validate-code

## URL Parameters

| code | string | Membership scheme code that is provided by Medical Management Systems to the client. |
| --- | --- | --- |

## Remarks

If the code is valid, HTTP status code is 2xx. Otherwise check exception (see Error handling).
