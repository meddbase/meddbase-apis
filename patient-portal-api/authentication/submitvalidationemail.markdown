---
layout: page
title: SubmitValidationEmail
nav_order: 16
parent: Authentication
---

# SubmitValidationEmail
{: .d-inline-block }

Deprecated
{: .label .label-red }

{: .deprecated }
Replaced with [SubmitActivationEmail](submitactivationemail)

Submits the confirmation key that the client retrieves from the URL and returns confirmation.

## JavaScript Library

```javascript
patientportal.auth.submitValidationEmail({
    key: 'key', 
    isOH: true
    });
```

## HTTP Method

| Verb | URL                                             |
|:-----|:------------------------------------------------|
| GET  | `/patientportalapi/auth/submit-validation-email`|


### URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| key       | string | Confirmation key that is included in the URL.               |
| is-oh     | bool   | True for the referral portal. False for the patient portal. |

### Returns

ActivationConfirmation

{: .note }
> If the activation is completed successfully the API returns the confirmation object. The confirmation may include the outstanding invoice (usually the membership fee) that should be paid. To pay for the invoice the client needs to call ProvidePayment method.
