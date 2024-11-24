---
layout: page
title: GetFeeds
nav_order: 1
parent: Feeds
---

# GetFeedsGets a number of the newest feeds.## JavaScript library method```patientportal.feed.getFeeds({toDate: &lt;to-date&gt;,referral:&lt;referral&gt;});```## HTTP MethodGET## ****Url****/patientportalapi/feed/feeds## URL Parameters| to-date | DateTime (optional) | Returns N feeds leading up to this date. N is server defined, but is likely to be between 10 - 20. Use this to implement infinite-scroll behaviour by passing the oldest date in the returned FeedData\[\] to subsequent calls to GetFeeds.<br><br>This also makes it easier to implement classic timeline based features of jumping to years, months, etc. || --- | --- | --- || referral | string (optional) | The key of the referral provided by the API upon GetReferrals. |## ReturnsFeedData\[\]## RemarksIf to-date is not used the server returns a number of the newest feeds but not all patient’s feeds.