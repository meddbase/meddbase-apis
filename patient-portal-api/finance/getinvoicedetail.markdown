---
layout: page
title: GetInvoiceDetail
nav_order: 2
parent: Finance
---

# GetInvoiceDetail

Returns an invoice.

## JavaScript library method

```javascript
patientportal.finance.getInvoiceDetail({
    invoice: <invoice>,
    invoiceNumber: <invoice-number>
});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/finance/invoice-detail

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| invoice | string (partially optional) | The key of the invoice provided by the API upon GetInvoices. |
| invoice-number | string (partially optional) | The invoice number provided by the API upon GetInvoices. |

## Returns

InvoiceData\[\]

## Remarks

One of optional parameters invoice or invoice-number must be used.
