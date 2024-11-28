---
layout: page
title: ActivationConfirmation
nav_order: 4
parent: Objects and data types
---

# ActivationConfirmation

Contains the information about the activated account.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| OutstandingInvoice | [InvoiceData](../objects-and-data-types/invoicedata) | The invoice the patient needs to pay. Usually the membership fee. Can be null if there is no outstanding invoice. |

## JSON Example

```json
{
    "OutstandingInvoice": {
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
            "Account": {
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
}
```
