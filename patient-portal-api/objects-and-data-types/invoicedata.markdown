---
layout: page
title: InvoiceData
nav_order: 40
parent: Objects and data types
---

# InvoiceData

Contains data of the invoice.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Key | string | Key of the invoice. |
| Date | DateTime | Date when was the invoice raised. |
| Number | int | Number of the invoice. The client can use it to provide a payment. |
| CurrencyCode | string | Three-letter currency code (e.g. "GBP", "EUR", "USD", etc.) |
| CurrencySymbol | string | Symbol for the currency |
| TotalNet | decimal |     |
| Tax | decimal |     |
| TotalGross | decimal |     |
| Paid | decimal | How much is already paid. |
| Items | InvoiceItemData\[\] | Invoice items. |
| CreditNotes | InvoiceCreditNoteData\[\] | Credit notes. |
| Creditor | InvoiceAddressData |     |
| Debtor | InvoiceAddressData |     |
| PayableOnline | bool | If the invoice is payable online (the billing company has an online payment account.) |

## JSON Example

```
{

"Key": "inv4645",

"Date": "2013-02-06",

"Number": "1865",

"CurrencyCode": "GBP",

"CurrencySymbol": "£",

"TotalNet": 200,

"Tax": 40,

"TotalGross": 240,

"Paid": 150,

"Creditor": {

"Name": "AXA PPP Healthcare",

"IsCompany": true,

"Address": {

"Address1": "44 Pall Mall",

"City": "London",

"PostCode": "SW1Y",

"Country": "United Kingdom"

},

"Account": {

"CODE": "AXA",

"Name": "AXA PPP Healthcare",

"Address": {

"Address1": "44 Pall Mall",

"City": "London",

"PostCode": "SW1Y",

"Country": "United Kingdom"

}

}

},

"Debtor": {

"Name": "Mr. John Lemon",

"IsCompany": false,

"Address": {

"Address1": "Studio 99",

"Address2": "Backlok Street",

"Address3": "Camden",

"City": "London",

"County": "",

"PostCode": "N1 7NK",

"Country": "United Kingdom"

},

Account: {

"Title": "Mr",

"Name": "John",

"Surname": "Lemon",

"SexType": 1,

"Initials": "JL",

"DateOfBirth": "1958-08-02T00:00:00",

"Mobile": "+444 895 523 411",

"Telephone": "+444 525 111 555",

"EmailAddress": "<john.lemon@test.com>",

"Address": {

"Address1": "Studio 99",

"Address2": "Backlok Street",

"Address3": "Camden",

"City": "London",

"County": "",

"PostCode": "N1 7NK",

"Country": "United Kingdom"

}

}

},

"PayableOnline": true

}
```
