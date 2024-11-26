---
layout: page
title: ServiceData
nav_order: 79
parent: Objects and data types
---

# ServiceData

Information about the Service.

## Properties

| Key | int | Unique key of the service. |
| --- | --- | --- |
| Code | string | Code of the service |
| Name | string | Name of the service |
| CurrencyCode | string | Code of the currency |
| CurrencySymbol | string | Symbol for the currency |
| NetPrice | decimal | Net price of the service |
| Tax | decimal | Tax on the service |
| GrossPrice | decimal | Gross price |
| ServiceType | [ServiceTypeData](#_ServiceTypeData) | Type of the service |

## JSON Example

```
{

"Code": "A1250",

"CurrencyCode":"GBP",

"CurrencySymbol": "£",

"GrossPrice": 0,

"Key":593,

"Name": "Creation of subcutaneous cerebrospinal fluid reservoir",

"NetPrice": 0,

"Tax": 0,

"ServiceType" : {

"Key": 84,

"Name": "Blood profile"

}

}
```
