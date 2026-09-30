---
layout: page
title: PurchaseResultData
nav_order: 106
parent: Objects and data types
---

# PurchaseResultData

The result of a course purchase.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Course | [PatientCourseOverviewData](../objects-and-data-types/patientcourseoverviewdata) | The new patient course. |
| Invoice | [InvoiceData](../objects-and-data-types/invoicedata) (optional) | The invoice for the purchase. It is not present if no invoice was raised. |

## JSON Example

```json
{
    "Course": {
        "Key": "8ebb55f10382d73e494e7207d1bd7272",
        "CourseKey": "c31a0f7e2b94d5581e6f70a3b2c49d10",
        "Code": "EHP",
        "Name": "Executive Health Programme",
        "PublicNotes": "Annual health programme.",
        "FirstIncludedDay": "2026-10-01",
        "LastIncludedDay": "2027-09-30",
        "Status": "Active"
    },
    "Invoice": {
        "Key": "5d1b7c0a44e29f63a8b1d20e7c93f455",
        "Date": "2026-09-30T10:15:00",
        "Number": 40219,
        "CurrencyCode": "GBP",
        "CurrencySymbol": "£",
        "TotalNet": 1250.0,
        "Tax": 250.0,
        "TotalGross": 1500.0,
        "Paid": 0.0,
        "PayableOnline": true
    }
}
```
