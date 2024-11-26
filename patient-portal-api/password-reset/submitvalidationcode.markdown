---
layout: page
title: SubmitValidationCode
nav_order: 4
parent: Password reset
---

# SubmitValidationCode

Submits the validation code for a specific password reset key. Returns a new Session ID the client could use to set a new password.

## JavaScript library method

```javascript
patientportal.passwordReset.submitValidationCode({ key: <key>, code: <code> });
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/password-reset/submit-validation-code` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| is-oh | bool | True for the referral portal. False for the patient portal. |

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| key | key | The password reset key. |
| code | code | The validation code. |

## Remarks

Submitting the validation code creates a temporary security context which is valid for 15 minutes. Within this time frame the patient must complete the password reset process.

The client may use ValidateKey to verify whether the security context runs out and request new validation code to create a new security context.

If something goes wrong please check exception (see Error handling).

## Returns

The SessionId is used to establish a security context via ASP.NET_SessionId cookie parameter.

```
{

"SessionId":"R9I8Dr8rGQcQ6EOfxVyOBX2r8zt4KTO06vW0O2+GyFc="

}
```
