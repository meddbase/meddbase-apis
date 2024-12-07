---
layout: page
title: Cancel
nav_order: 7
parent: Referrals
---

# Cancel

Cancels the referral.

## JavaScript library method

```javascript
patientportal.referrals.cancel({
    referral: <referral>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/referrals/cancel` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| referral | string | The key of the referral provided by the API upon [GetReferrals](../referrals/getreferrals). |

## Returns

[ReferralData](../objects-and-data-types/referraldata)
