---
layout: page
title: SendValidationSMS
nav_order: 17
parent: Authentication
---

# SendValidationSMS
{: .d-inline-block }

Deprecated
{: .label .label-red }

{: .deprecated }
Replaced with [SendActivationSMS](sendactivationsms)

Sends the validation SMS to the patient’s mobile telephone number.

## JavaScript Library

```javascript
patientportal.auth.sendValidationSMS({
    mobile: 'mobile',
    isOH: true
});
```

## HTTP Method

| Verb | URL                                           |
|:-----|:----------------------------------------------|
| GET  | `/patientportalapi/auth/send-validation-sms`  |

### URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| mobile    | string | Patient’s mobile telephone number.                          |
| is-oh     | bool   | True for the referral portal. False for the patient portal. |

{: .note }
> Sometimes the patient needs to send the validation SMS again because (for example) she deletes it before activating her account.
