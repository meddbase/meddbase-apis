---
layout: page
title: CurrentMembershipSchemeData
nav_order: 26
parent: Objects and data types
---

# CurrentMembershipSchemeData

Provides information about the current membership scheme of the patient.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Name | string | Name of the scheme. |
| Code | string | Membership code of the scheme. |
| BillingFrequency | string | Billing frequency of current scheme. Weekly, monthly, etc. |
| CurrencyCode | string | Three-letter currency code (e.g. "GBP", "EUR", "USD", etc.) |
| CurrencySymbol | string | Symbol for the currency |
| NetPrice | decimal |     |
| Tax | decimal |     |
| GrossPrice | decimal |     |
| RequiresOnlinePayment | bool | Scheme requires an online recurring payment method set up |
| OnlinePaymentAllowed | bool | The scheme allows online recurring payments. |
| JoinedDateTime | DateTime | The date patient joined the scheme. |
| NextInvoiceDateTime | DateTime | Date of next billing cycle |
| OnlinePaymentMethod | string | Associated online payment method (formatted string) |
| LastInvoiceBalance | decimal | Balance on the last invoice for the memberhsip |
| LastInvoiceKey | string | Encrypted key of the last invoice. |

## JSON Example

```json
{
    "Name": "Basic Membership Program",
    "Code": "ms001",
    "BillingFrequency": "Monthly",
    "CurrencyCode": "GBP",
    "CurrencySymbol": "£",
    "NetPrice": 100,
    "Tax": 20,
    "GrossPrice": 120,
    "RequiresOnlinePayment": false,
    "OnlinePaymentAllowed": false,
    "JoinedDateTime": "2016-12-16T16:13:40.747",
    "NextInvoiceDateTime": "2017-01-17T00:00:00",
    "OnlinePaymentMethod": "VISA (****0014) Expiry: 01/28",
    "LastInvoiceBalance": 160,
    "LastInvoiceKey": "2e0bba51a59f90a4c23be92ca6c89b0a"
}
```
