---
layout: page
title: AddMessage
nav_order: 4
parent: Feeds
---

# AddMessage

Adds a new message to the existing feed.

## JavaScript library method

```javascript
patientportal.feed.addMessage({
    feed : <feed>,
    messageText: <messageText>,
    referral:<referral>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/feed/add-message` |

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| feed | string | Key of the feed provided by the API upon [GetFeeds](../feeds/getfeeds). |
| messageText | string | Text of the new message. Text can be formatted as HTML or plain text. |
| referral | string (optional) | The key of the referral provided by the API upon [GetReferrals](../referrals/getreferrals). |
