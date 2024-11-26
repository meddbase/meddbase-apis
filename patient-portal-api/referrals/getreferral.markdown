---
layout: page
title: GetReferral
nav_order: 2
parent: Referrals
---

# GetReferral

Returns the referral full details.

## JavaScript library method

```javascript
patientportal.referrals.getReferral({
    referral: <referral>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/referrals/referral` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| referral | string | The key of the referral provided by the API upon GetReferrals. |

## Returns

ReferralData
