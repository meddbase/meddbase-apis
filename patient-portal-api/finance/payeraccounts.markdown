---
layout: page
title: PayerAccounts
nav_order: 5
parent: Finance
---

# PayerAccounts

Returns a list of existing stored cards for the current logged in person, which they can use for a new payment. Returns an empty list, if no stored cards exist for the logged in person (payer).

## JavaScript library method

```javascript
patientportal.finance.prototype.payerAccounts(invoiceKey: <invoice-key>)
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/payment-gateway/payer-accounts` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| invoice-key | int | Encrypted Key of the invoice provided by the API. (Optional). If provided, the payer accounts are filtered by the portal payment type for that invoice. This should always be provided for online payments, and removed for payer account management. |

## Returns

[PayerAccountData](#_PayerAccountData_1)\[\]
