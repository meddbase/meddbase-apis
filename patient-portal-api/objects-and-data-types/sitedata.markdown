---
layout: page
title: SiteData
nav_order: 83
parent: Objects and data types
---

# SiteData

Geographic place/residence of the doctor/clinic.

## Properties

| Key | int | Key of site. |
| --- | --- | --- |
| Name | string | Name of the site. |
| Address | AddressData | Address of the site. |
| Locations | LocationData\[\] | Possible locations within this site.<br><br>Note: Sometimes the location may be placed on geographically different place than the site. To show the location the client should use the location’s address. |

## JSON Example

```
{

"Key": 1123,

"Name": "2CP (Eye Room)",

"Address":{

"Address1": "2 Clifton Park Ave",

"Address2": "",

"Address3": "",

"City": "London",

"County": "",

"PostCode": "SW20 8BD",

"Country": "United Kingdom"

},

"Locations": \[

{

"Key": 45,

"Name": "Surgery"

},

{

"Key": 214,

"Name": "Room 1"

}

\]

}
```
