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

## Returned JSON

```
[AddressData](../objects-and-data-types/addressdata)
```

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

## Returned JSON

AddressData

Patient section (or any other) to gather details about the patient.

It is recommended to provide Login button within the UI so the user could login if they already have an account. This way you avoid unnecessary duplicate records that could be created in the system.
