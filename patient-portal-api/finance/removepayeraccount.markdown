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
patientportal.finance.prototype.removePayerAccount({
    payerAccountKey: <payer-account-key>
})
```

## HTTP Method

GET

## ****Url****

/patientportalapi/payment-gateway/remove-payer-account

## URL Parameters

| payer-account-key | int | Payer Account Key of the account to be disabled as retrieved from [PayerAccounts](#_PayerAccounts) |
| --- | --- | --- |

## Returns

bool
