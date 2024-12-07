---
layout: page
title: Address
nav_order: 3
parent: Address Finder
---

# Address

Returns address details for the provided encrypted key.

## JavaScript library method

```javascript
patientportal.addressFinder.address({key: <key>});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/address-finder/address` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| key | string | An encrypted key value containing partial address information. |

## Returns

[AddressData](../objects-and-data-types/addressdata)

## Returned JSON

```json
{
    "status": "ok",
    "result": {
        "Address1": "127 Northchurch Rd",
        "Address2": "Borough of Islington",
        "Address3": "",
        "City": "London",
        "County": "",
        "PostCode": "N1 3PA",
        "Country": "United Kingdom"
    }
}
```