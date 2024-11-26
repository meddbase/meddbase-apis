---
layout: page
title: ContactDemographicData
nav_order: 23
parent: Objects and data types
---

# ContactDemographicData

Contains the contact’s demographic information.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Title | string |     |
| Name | string |     |
| Details | string |     |
| Fax | string |     |
| Mobile | string |     |
| Telephone | string |     |
| EmailAddress | string |     |
| Address | AddressData |     |

## JSON Example

```
{

"Title": "Mr",

"Name": "Robert Murian",

"Mobile": "0795523411",

"Telephone": "+444 525 111 555",

"EmailAddress": "<robert@comp.com>",

"Address": {

"Address1": "Pall Mall",

"Address2": "",

"Address3": "",

"City": "London",

"County": "",

"PostCode": "SW1Y",

"Country": "United Kingdom"

}

}
```
