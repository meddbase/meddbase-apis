---
layout: page
title: GetFeeds
nav_order: 1
parent: Feeds
---

# GetFeeds

Gets a number of the newest feeds.

## JavaScript library method

```javascript
patientportal.feed.getFeeds({
    toDate: <to-date>,
    referral:<referral>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/feed/feeds` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| to-date | DateTime (optional) | Returns N feeds leading up to this date. N is server defined, but is likely to be between 10 - 20. Use this to implement infinite-scroll behaviour by passing the oldest date in the returned [FeedData](../objects-and-data-types/feeddata)[] to subsequent calls to [GetFeeds](../feeds/getfeeds).<br><br>This also makes it easier to implement classic timeline based features of jumping to years, months, etc. |
| referral | string (optional) | The key of the referral provided by the API upon [GetReferrals](../referrals/getreferrals). |

## Returns

[FeedData](../objects-and-data-types/feeddata)[]

## Remarks

If to-date is not used the server returns a number of the newest feeds but not all patient’s feeds.
