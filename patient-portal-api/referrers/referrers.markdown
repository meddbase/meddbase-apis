---
layout: page
title: Referrers
nav_order: 33
parent: Patient Portal API
---

# Referrers

Returns a list of the available referrers to select from when updating the patient’s details.

## JavaScript library method

```javascript
patientportal.referrers.getReferrers();
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/referrers/referrers` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Key | string | The absence key. |

## Returns

[ReferrerData](../objects-and-data-types/referrerdata)[]
