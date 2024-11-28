---
layout: page
title: SendInvoiceByEmail
nav_order: 3
parent: Finance
---

# SendInvoiceByEmail

Sends the specific invoice to the patient’s email address.

## JavaScript library method

```javascript
patientportal.finance.sendInvoiceByEmail({invoiceNumber: <invoice-number>});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/finance/send-by-email` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| invoice-number | string | The invoice number provided by the API upon GetInvoices. |

## Remarks

The client should show a warning message that sending an invoice over email isn't encrypted and that the patient should use this feature at their own risk. If online payment is active, the email contains a link to the portal to pay online for unpaid invoices. The link is in the following format:

`https://{portal}/pay?invoiceKey={encrypted invoice key}`

The invoice key can be used in logged-in or anonymous mode to process payment using [ProvidePayment](#_ProvidePayment).
