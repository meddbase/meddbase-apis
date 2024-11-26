---
layout: page
title: AddressData
nav_order: 5
parent: Objects and data types
---

# AddressData

Address of the patient/company.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Address1 | string |     |
| Address2 | string |     |
| Address3 | string |     |
| City | string |     |
| County | string |     |
| PostCode | string |     |
| Country | string |     |
| Distance | decimal | Distance in miles from another geographical coordinate. Used within GetSites to provide distance from patient’s home/work address or GPS coordinate. |

## JSON Example

```
{

"Address1": "127 Northchurch Rd",

"Address2": "Borough of Islington",

"Address3": "",

"City": "London",

"County": "",

"PostCode": "N1 3PA",

"Country": "United Kingdom",

}
```
