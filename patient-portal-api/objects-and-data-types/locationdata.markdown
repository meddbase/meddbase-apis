---
layout: page
title: LocationData
nav_order: 43
parent: Objects and data types
---

# LocationData

The location within the site.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Key | int |     |
| Name | string |     |
| Address | [AddressData](../objects-and-data-types/addressdata) |     |

## JSON Example

```json
{
    "Key": 214,
    "Name": "Room 1",
    "Address": {
        "Address1": "2 Clifton Park Ave",
        "Address2": "",
        "Address3": "",
        "City": "London",
        "County": "",
        "PostCode": "SW20 8BD",
        "Country": "United Kingdom"
    }
}
```
