---
layout: page
title: GetFeed
nav_order: 2
parent: Feeds
---

# GetFeed

Gets a specific feed.

## JavaScript library method

```
patientportal.feed.getFeed({

feed: &lt;feed&gt;,

referral:&lt;referral&gt;

});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/feed/feed

## URL Parameters

| feed | string | Key of the feed provided by the API upon GetFeeds. |
| --- | --- | --- |
| referral | string (optional) | The key of the referral provided by the API upon GetReferrals. |

## Returns

FeedData
