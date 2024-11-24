---
layout: page
title: AddMessage
nav_order: 4
parent: Feeds
---

# AddMessageAdds a new message to the existing feed.## JavaScript library method```patientportal.feed.addMessage({feed : &lt;feed&gt;,messageText: &lt;messageText&gt;,referral:&lt;referral&gt;});```## HTTP MethodPOST## ****Url****/patientportalapi/feed/add-message## POST Parameters| feed | string | Key of the feed provided by the API upon GetFeeds. || --- | --- | --- || messageText | string | Text of the new message. Text can be formatted as HTML or plain text. || referral | string (optional) | The key of the referral provided by the API upon GetReferrals. |