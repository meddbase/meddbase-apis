---
layout: page
title: SubmitValidationSMS
nav_order: 18
parent: Authentication
---

# SubmitValidationSMS
{: .d-inline-block }

Deprecated
{: .label .label-red }

{: .deprecated }
Replaced with [SubmitActicationSMS](submitacticationsms)

Submits the validation number from the validation SMS and returns confirmation.

## JavaScript Library

```javascript
patientportal.auth.submitValidationSMS({
    code: 'code',
    mobile: 'mobile',
    isOH: true
});
```

## HTTP Method

| Verb | URL                                           |
|:-----|:----------------------------------------------|
| GET  | `/patientportalapi/auth/submit-validation-sms`|

### URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| code      | string | Validation code.                                            |
| mobile    | string | Patient’s mobile telephone number.                          |
| is-oh     | bool   | True for the referral portal. False for the patient portal. |

### Returns

ActivationConfirmation

{: .note }
> If the activation is completed successfully the API returns the confirmation object. The confirmation may include the outstanding invoice (usually the membership fee) that should be paid. To pay for the invoice the client needs to call ProvidePayment method.
