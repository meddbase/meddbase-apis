---
layout: page
title: GetInvoices
nav_order: 1
parent: Finance
---

# GetInvoices

Returns a number of invoices according given filters.

## JavaScript library method

```javascript
patientportal.finance.getInvoices({
    toDate: <to-data>,
    paid: <paid>
});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/finance/invoices

## URL Parameters

| to-date | DateTime (optional) | Returns N invoices leading up to this date. N is server defined, but is likely to be between 10 - 20. Use this to implement infinite-scroll behaviour by passing the oldest date in the returned InvoiceData\[\] to subsequent calls to GetInvoices.<br><br>This also makes it easier to implement classic timeline based features of jumping to years, months, etc. |
| --- | --- | --- |
| paid | bool (optional) | True to get only paid invoices, false to get only unpaid and partially paid invoices, null (not present) to get all types of invoices (paid, partially paid and unpaid. |

## Returns

InvoiceData\[\]

## Remarks

If no optional (filter) parameters are present the server returns all unpaid and partially paid invoices and a number of paid invoices.
