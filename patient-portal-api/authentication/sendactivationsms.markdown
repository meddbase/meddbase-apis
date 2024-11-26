---
layout: page
title: SendActivationSMS
nav_order: 13
parent: Authentication
---

# SendActivationSMS

Sends the activation SMS to the patient’s mobile telephone number.

## JavaScript library method

```javascript
patientportal.auth.sendActivationSMS({isOH: <is-oh>});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/auth/send-activation-sms` |

## URL Parameters

| is-oh | bool | True for the referral portal. False for the patient portal. |
| --- | --- | --- |

## Remarks

Sometimes the patient needs to send the activation SMS again because (for example) she deletes it before activating her account.
