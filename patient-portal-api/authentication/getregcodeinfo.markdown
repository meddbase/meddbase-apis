---
layout: page
title: GetRegCodeInfo
nav_order: 7
parent: Authentication
---

# GetRegCodeInfo

Returns information for the online sign-up access code (i.e. charge band information, because the online sign-up access code is assigned to the charge band).

## JavaScript library method

```javascript
patientportal.auth.getRegCodeInfo({regCode: <reg-code>});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/auth/reg-code-info` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| reg-code | string | Online sign up access code that is provided to the patient. |
| is-oh | bool | True for the referral portal. False for the patient portal. |

## Returns

[ChargeBandData](../objects-and-data-types/chargebanddata)
