---
layout: page
title: SubmitActicationSMS
nav_order: 14
parent: Authentication
---

# SubmitActicationSMS

Submits the activation number from the activation SMS and returns confirmation.

## JavaScript library method

```javascript
patientportal.auth.submitActivationSMS({code: <code>, isOH: <is-oh>});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/auth/submit-activation-sms` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| is-oh | bool | True for the referral portal. False for the patient portal. |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| code | string | Activation code. |

## Returns

[ActivationConfirmation](../objects-and-data-types/activationconfirmation)

## Remarks

If the activation completes successfully the API returns the confirmation object. The confirmation may include the outstanding invoice (usually the membership fee) that should be paid. To pay for the invoice the client needs to call [ProvidePayment](../finance/providepayment) method.
