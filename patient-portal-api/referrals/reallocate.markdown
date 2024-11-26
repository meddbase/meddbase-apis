---
layout: page
title: Reallocate
nav_order: 9
parent: Referrals
---

# Reallocate

Re-allocate the referral to another user.

## JavaScript library method

```
patientportal.referrals.reallocate({

referral: &lt;referral&gt;,

user: &lt;user&gt;

});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/referrals/reallocate

## URL Parameters

| referral | string | The key of the referral provided by the API upon GetReferrals. |
| --- | --- | --- |
| user | string | The key of the user provided by the API upon FindUserToReallocate. |

## Returns

ReferralData
