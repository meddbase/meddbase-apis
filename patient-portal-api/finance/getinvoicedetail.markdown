---
layout: page
title: GetInvoiceDetail
nav_order: 2
parent: Finance
---

# GetInvoiceDetail

Returns an invoice.

## JavaScript library method

```
patientportal.finance.getInvoiceDetail({

invoice: &lt;invoice&gt;,

invoiceNumber: &lt;invoice-number&gt;

});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/finance/invoice-detail

## URL Parameters

| invoice | string (partially optional) | The key of the invoice provided by the API upon GetInvoices. |
| --- | --- | --- |
| invoice-number | string (partially optional) | The invoice number provided by the API upon GetInvoices. |

## Returns

InvoiceData\[\]

## Remarks

One of optional parameters invoice or invoice-number must be used.
