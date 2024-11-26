---
layout: page
title: SendValidationSMS
nav_order: 3
parent: Password reset
---

# SendValidationSMS

Sends a validation code for a specific password reset key to the mobile number.

## JavaScript library method

```
patientportal.passwordReset.sendValidationSMS({ key: &lt;key&gt; });
```

## HTTP Method

POST

## ****Url****

/patientportalapi/password-reset/send-validation-sms

## URL Parameters

| is-oh | bool | True for the referral portal. False for the patient portal. |
| --- | --- | --- |

## POST Parameters

| key | key | The password reset key. |
| --- | --- | --- |
