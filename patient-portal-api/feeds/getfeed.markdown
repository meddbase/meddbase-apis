---
layout: page
title: GetFeed
nav_order: 2
parent: Feeds
---

# GetFeed

Gets a specific feed.

## JavaScript library method

```javascript
patientportal.feed.getFeed({
    feed: <feed>,
    referral:<referral>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/feed/feed` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| feed | string | Key of the feed provided by the API upon GetFeeds. |
| referral | string (optional) | The key of the referral provided by the API upon GetReferrals. |

## Returns

FeedData
