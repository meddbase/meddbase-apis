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

POST

## Url

/patientportalapi/auth/submit-2fa-code

## POST Parameters

| code | string | 2FA code. |
| --- | --- | --- |

## Returns

AuthenticationData
