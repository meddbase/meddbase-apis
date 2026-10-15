---
layout: page
title: PayerCoursesData
nav_order: 103
parent: Objects and data types
---

# PayerCoursesData

The courses that can be bought with one payer type.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| PayerType | [PayerType](../objects-and-data-types/payertype) | The payer type. Use its `Key` in the `payer-type` parameter of [GetCourse](../courses/getcourse) and [Purchase](../courses/purchase). |
| Services | [CourseOverviewData](../objects-and-data-types/courseoverviewdata)[] | The courses that can be bought with this payer type. The prices are the prices for this payer type. |

## JSON Example

```json
{
    "PayerType": {
        "Key": "PA",
        "Name": "Self pay"
    },
    "Services": [
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
            }
        }
    ]
}
```
