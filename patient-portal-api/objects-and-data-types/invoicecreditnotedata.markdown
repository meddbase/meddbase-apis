---
layout: page
title: InvoiceCreditNoteData
nav_order: 39
parent: Objects and data types
---

# InvoiceCreditNoteData

Contains information from one credit note of an invoice.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Key | string | Key of the item. |
| Date | [DateTime](../objects-and-data-types/datetime) | When was a credit note raised. |
| ServiceName | string | Name of the service the credit note was raised for.<br><br>If empty the credit note is raised for whole invoice. |
| Comments | string | A reason why was this credit note raised. |
| CurrencyCode | string | Three-letter currency code (e.g. "GBP", "EUR", "USD", etc.) |     |
| CurrencySymbol | string | Symbol for the currency |     |
| NetPrice | decimal |     |     |
| Tax | decimal |     |     |
| GrossPrice | decimal |     |     |

## JSON Example

```json
{
    "Key": "156480",
    "Date": "2013-10-05T00:00:00",
    "ServiceName": "Consultation",
    "Comments": "Cancellation",
    "CurrencyCode": "GBP",
    "CurrencySymbol": "£",
    "NetPrice": 100,
    "Tax": 20,
    "GrossPrice": 120
}
```
