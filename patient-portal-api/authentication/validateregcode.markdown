---
layout: page
title: ValidateRegCode
nav_order: 6
parent: Authentication
---

# ValidateRegCode

Confirms the validity of the online sign up access code.

## JavaScript library method

```javascript
patientportal.auth.validateRegCode({
    regCode: <reg-code>,
    isOH: <is-oh>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/auth/validate-reg-code` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| reg-code | string | Online sign up access code that is provided to the patient. |
| is-oh | bool | True for the referral portal. False for the patient portal. |

## Returns

[ChargeBandData](../objects-and-data-types/chargebanddata)

## Remarks

If the registration code is invalid, check the exception (see [Error handling](../error-handling/error-handling)).
