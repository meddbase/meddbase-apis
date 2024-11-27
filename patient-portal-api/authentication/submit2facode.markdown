---
layout: page
title: Submit2faCode
nav_order: 29
parent: Authentication
---

# Submit2faCode

Submits 2FA code and completes profile login.

## JavaScript library method

```javascript
patientportal.auth.submit2faCode({code: <code>});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/auth/submit-2fa-code` |

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| code | string | 2FA code. |

## Returns

[AuthenticationData](../objects-and-data-types/authenticationdata)
