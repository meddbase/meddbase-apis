---
layout: page
title: CourseData
nav_order: 93
parent: Objects and data types
---

# CourseData

A course as the chamber sells it, with its credit allowances. It has all the properties of [CourseOverviewData](../objects-and-data-types/courseoverviewdata) and the property `CreditAllowances`.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Key | string | Key of the course. Use it in the `course` parameter of [GetCourse](../courses/getcourse) and [Purchase](../courses/purchase). |
| Code | string | Code of the course. |
| Name | string | Name of the course. |
| CurrencyCode | string | Three-letter currency code (e.g. "GBP", "EUR", "USD", etc.) |
| CurrencySymbol | string | Symbol for the currency. |
| NetPrice | decimal | Net price of the course. |
| Tax | decimal | Tax on the course. |
| GrossPrice | decimal | Gross price of the course. |
| PublicNotes | string | Notes about the course for the patient. |
| Expiration | [PeriodData](../objects-and-data-types/perioddata) | How long a patient course is valid after its start date. All the values are 0 if the course does not expire. |
| CreditAllowances | [CreditAllowanceData](../objects-and-data-types/creditallowancedata)[] | The credits that the course gives. |

## JSON Example

```json
{
    "Key": "c31a0f7e2b94d5581e6f70a3b2c49d10",
    "Code": "EHP",
    "Name": "Executive Health Programme",
    "CurrencyCode": "GBP",
    "CurrencySymbol": "£",
    "NetPrice": 1250.0,
    "Tax": 250.0,
    "GrossPrice": 1500.0,
    "PublicNotes": "Annual health programme.",
    "Expiration": {
        "Years": 1,
        "Months": 0,
        "Days": 0
    },
    "CreditAllowances": [
        {
            "Type": "Fixed",
            "ActivePeriod": {
                "FirstIncludedDay": "2026-07-01",
                "LastIncludedDay": "2027-06-30"
            },
            "Services": [
                {
                    "ServiceKey": 501,
                    "ServiceName": "Physiotherapy",
                    "Credits": 6,
                    "PublicNotes": "",
                    "ServiceType": {
                        "Code": "A",
                        "Name": "Appointment"
                    }
                }
            ]
        }
    ]
}
```
