---
layout: page
title: ValidateKey
nav_order: 2
parent: Password reset
---

# ValidateKey

Validates the password reset key that is included in the URL sent via the email in the previous API method.

## JavaScript library method

```javascript
patientportal.passwordReset.validateKey({ key: <key> });
```

## HTTP Method

POST

## ****Url****

/patientportalapi/password-reset/validate-key

## URL Parameters

| is-oh | bool | True for the referral portal. False for the patient portal. |
| --- | --- | --- |

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| key | key | The password reset key. |

## Returns

The method either fails with an exception message (e.g. Link expired) or it passes and tells you what method is used to verify the patient/manager.

- SMSVerfication – we verify via a validation code that is sent to the mobile number
  - Use MobileHint as so the patient can partially verify what mobile number is going to be used.
- DemographicsVerification – we verify via a full demographics match
  - Note this method is not recommended and will be removed in future. It is supported until all clients move to SMS verification.

```
{

"SMSVerification": true,

"DemographicsVerification": false,

"MobileHint": "xxxxxxxx569"

}
```
