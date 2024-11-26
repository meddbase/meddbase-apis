---
layout: page
title: SubmitActicationSMS
nav_order: 14
parent: Authentication
---

# SubmitActicationSMS

Submits the activation number from the activation SMS and returns confirmation.

## JavaScript library method

```
patientportal.auth.submitActivationSMS({code: &lt;code&gt;, isOH: &lt;is-oh&gt;});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/auth/submit-activation-sms

## URL Parameters

| is-oh | bool | True for the referral portal. False for the patient portal. |
| --- | --- | --- |

## URL Parameters

| code | string | Activation code. |
| --- | --- | --- |

## Returns

ActivationConfirmation

## Remarks

If the activation completes successfully the API returns the confirmation object. The confirmation may include the outstanding invoice (usually the membership fee) that should be paid. To pay for the invoice the client needs to call ProvidePayment method.
