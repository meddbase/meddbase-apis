---
layout: page
title: FollowUp
nav_order: 11
parent: Referrals
---

# FollowUp

Sends the follow up referral.

## JavaScript library method

```javascript
patientportal.referrals.followUp({
    referral: <referral>,
    reason: <reason>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/referrals/follow-up` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| referral | string | The key of the referral provided by the API upon GetReferrals. |

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| reason | string | The reason why the user sends the follow up referral. |

## Returns

[ReferralData](../objects-and-data-types/referraldata)
