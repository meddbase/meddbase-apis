---
layout: page
title: SetPassword
nav_order: 5
parent: Password reset
---

# SetPassword

Sets the new password. This is used if the SMS verification method (see previous API calls) has been used.

## JavaScript library method

```
patientportal.passwordReset.setPassword({ key: &lt;key&gt;, newPassword: &lt;newPassword&gt; });
```

## HTTP Method

POST

## ****Url****

/patientportalapi/password-reset/set-password

## URL Parameters

| is-oh | bool | True for the referral portal. False for the patient portal. |
| --- | --- | --- |

## POST Parameters

| key | key | The password reset key. |
| --- | --- | --- |
| newPassword | newPassword | The new password. |

## Remarks

Please remember to provide ASP.NET_SessionId cookie with the session ID provided provided upon SubmitValidationCode.
