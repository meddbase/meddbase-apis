---
layout: page
title: InvoiceItemData
nav_order: 41
parent: Objects and data types
---

# InvoiceItemData

Contains information from one row of an invoice.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Key | string | Key of the item. |
| TypeName | string | Full name of the item type (e.g. Appointment, Module, Product, etc.). Item type specify a group that the item belongs to. |
| Name | string | Name of the item. |
| Code | string | Code of the item. |
| CurrencyCode | string | Three-letter currency code (e.g. "GBP", "EUR", "USD", etc.) |     |
| CurrencySymbol | string | Symbol for the currency |     |
| NetPrice | decimal |     |     |
| Tax | decimal |     |     |
| GrossPrice | decimal |     |     |

## JSON Example

```
{

"Key": "5642",

"TypeName": "Appointment",

"Name": "Consultation",

"Code": "123",

"CurrencyCode": "GBP",

"CurrencySymbol": "£",

"NetPrice": 100,

"Tax": 20,

"GrossPrice": 120,

}
```
