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
    referral: <referral>,
});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/referrals/send

## URL Parameters

| referral | string | The key of the referral provided by the API upon GetReferrals. |
| --- | --- | --- |

## Returns

ReferralData
