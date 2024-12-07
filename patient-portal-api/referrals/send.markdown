---
layout: page
title: Send
nav_order: 6
parent: Referrals
---

# Send

Sends the referral.

## JavaScript library method

```javascript
patientportal.referrals.send({
    referral: <referral>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/referrals/send` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| referral | string | The key of the referral provided by the API upon [GetReferrals](../referrals/getreferrals). |

## Returns

[ReferralData](../objects-and-data-types/referraldata)
