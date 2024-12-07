---
layout: page
title: SubmitActivationEmail
nav_order: 12
parent: Authentication
---

# SubmitActivationEmail

Submits the activation key that the client retrieves from the URL and returns confirmation.

## JavaScript library method

```javascript
patientportal.auth.submitActivationEmail({isOH: <is-oh>});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/auth/submit-validation-email` |

## GET Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| is-oh | bool | True for the referral portal. False for the patient portal. |

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| key | string | Confirmation key that is included in the URL. |

## Returns

[ActivationConfirmation](../objects-and-data-types/activationconfirmation)

## Remarks

If the activation completes successfully the API returns the confirmation object. The confirmation may include the outstanding invoice (usually the membership fee) that should be paid. To pay for the invoice the client needs to call [ProvidePayment](../finance/providepayment) method.
