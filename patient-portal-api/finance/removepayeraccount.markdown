---
layout: page
title: RemovePayerAccount
nav_order: 6
parent: Finance
---

# RemovePayerAccount

Removes (disables) an existing stored card for the current logged in person.

## JavaScript library method

```javascript
patientportal.finance.removePayerAccount({
    payerAccountKey: <payer-account-key>
})
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/payment-gateway/remove-payer-account` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| payer-account-key | int | Payer Account Key of the account to be disabled as retrieved from [PayerAccounts](#_PayerAccounts) |

## Returns

bool
