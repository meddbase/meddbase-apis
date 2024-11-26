---
layout: page
title: PayerAccounts
nav_order: 5
parent: Finance
---

# PayerAccounts

Returns a list of existing stored cards for the current logged in person, which they can use for a new payment. Returns an empty list, if no stored cards exist for the logged in person (payer).

## JavaScript library method

```
patientportal.finance.prototype.payerAccounts(invoiceKey: &lt;invoice-key&gt;)
```

## HTTP Method

GET

## ****Url****

/patientportalapi/payment-gateway/payer-accounts

## URL Parameters

| invoice-key | int | Encrypted Key of the invoice provided by the API. (Optional). If provided, the payer accounts are filtered by the portal payment type for that invoice. This should always be provided for online payments, and removed for payer account management. |
| --- | --- | --- |

## Returns

[PayerAccountData](#_PayerAccountData_1)\[\]
