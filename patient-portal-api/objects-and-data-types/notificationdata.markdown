---
layout: page
title: NotificationData
nav_order: 49
parent: Objects and data types
---

# NotificationData

Provides information about notification (outstanding invoice or questionnaire, etc.).

## Properties

<table><tbody><tr><th><p>Key</p></th><th><p>string</p></th><th><p>Key of the notification.</p></th></tr><tr><td><p>Type</p></td><td><p>int</p></td><td><p>The type of the notification:</p><ul><li>1 = Appointment coming up soon</li><li>2 = Outstanding questionnaire</li><li>4 = Outstanding invoice</li><li>8 = Outstanding messages</li><li>16 = Action required</li><li>32 = Referral notification</li></ul></td></tr><tr><td><p>Message</p></td><td><p>string</p></td><td><p>Message of the notification.</p></td></tr><tr><td><p>ObjectKey</p></td><td><p>string</p></td><td><p>Key of the related object to this notification according to the Type of the notification (e.g. notification of type 2 ‘Outstanding questionnaire’ relates to the questionnaire so the object key means the questionnaire key.</p><p>By the Type the ObjectKey means:</p><ul><li>1 = appointment key</li><li>2 = questionnaire key</li><li>4 = invoice key</li><li>8 = feed key</li><li>16 =<ul><li>‘SetContactOptions’ to force patient to set their contact options.</li><li>‘AcceptTermsAndConditions’ to force patient to re-accept the Terms and conditions.</li></ul></li><li>32 = referral key</li></ul><p>The client can use this key to redirect/show more details about related objects.</p></td></tr></tbody></table>

## JSON Example

```
{

"Key": "2-1568",

"Type": 1,

"Message": "You need to complete pre-medical questionnaire.",

"ObjectKey": "1568"

}
```
