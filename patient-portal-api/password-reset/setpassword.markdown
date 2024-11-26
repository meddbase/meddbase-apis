---
layout: page
title: SetPassword
nav_order: 5
parent: Password reset
---

# SetPassword

Sets the new password. This is used if the SMS verification method (see previous API calls) has been used.

## JavaScript library method

```javascript
patientportal.passwordReset.setPassword({ key: <key>, newPassword: <newPassword> });
```

## HTTP Method

POST

## ****Url****

/patientportalapi/password-reset/set-password

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| is-oh | bool | True for the referral portal. False for the patient portal. |

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| key | key | The password reset key. |
| newPassword | newPassword | The new password. |

## Remarks

Please remember to provide ASP.NET_SessionId cookie with the session ID provided provided upon SubmitValidationCode.
