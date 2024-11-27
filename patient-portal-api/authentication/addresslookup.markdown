---
layout: page
title: AddressLookup
nav_order: 22
parent: Authentication
---

# AddressLookup
{: .d-inline-block }

Deprecated
{: .label .label-red }

{: .deprecated }
See [Address Finder](../address-finder/address-finder) section for more details.
Returns a number of possible address for the postcode.

## JavaScript Library

```javascript
patientportal.auth.addressLookup({
    postcode: 'postcode',
    house: 'house'
});
```

## HTTP Method

| Verb | URL                                    |
|:-----|:---------------------------------------|
| GET  | `/patientportalapi/auth/address-lookup`|

## URL Parameters

| Parameter | Type   | Required | Description                                                    |
|:----------|:-------|:---------|:---------------------------------------------------------------|
| postcode  | string | Yes      | Case-insensitive postcode without space (e.g. N70NH or n70nh). |
| house     | string | No       | House name or house number.                                    |

## Returns

[AddressData](../objects-and-data-types/addressdata)[]
