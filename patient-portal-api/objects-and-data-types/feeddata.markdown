---
layout: page
title: FeedData
nav_order: 34
parent: Objects and data types
---

# FeedData

Feed of the feeds system.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Key | string | Key of the feed. |
| StartDate | [DateTime](../objects-and-data-types/datetime) | Day and time when the feed was created. |
| AuthorName | string | Name of the author who created this feed. |
| LastMessage | [FeedMessageData](../objects-and-data-types/feedmessagedata) | The last message only. |
| Messages | [FeedMessageData](../objects-and-data-types/feedmessagedata)[] | All messages sorted by date descending. The message on the first position is the latest message of the feed. |
| OutstandingMessageNotification | [NotificationData](../objects-and-data-types/notificationdata) | Outstanding message notification is present if there is a new message in the feed. Property is null or undefined if there is no new message in the feed.<br><br>Use ConfirmNotification provided by the API to confirm this notification. |

## JSON Example

```json
{
    "Key": "f562874",
    "StartDate": "2013-08-02T14:45:58.9525711+01:00",
    "AuthorName": "Dr. Ben",
    "LastMessage": {
        "AuthorName": "Dr. Ben",
        "Date": "2013-08-02T14:55:15.1875264+01:00",
        "Text": "<div>Thanks John</div>"
    },
    "Messages": [
        {
            "AuthorName": "Dr. Ben",
            "Date": "2013-08-02T14:55:15.1875264+01:00",
            "Text": "<div>Thanks John</div>"
        },
        {
            "AuthorName": "John",
            "Date": "2013-08-02T14:50:05.5684528+01:00",
            "Text": "Yes, I can."
        },
        {
            "AuthorName": "Dr. Ben",
            "Date": "2013-08-02T14:45:58.9525711+01:00",
            "Text": "<div><b>Hi John, could you...</b></div>"
        }
    ],
    "OutstandingMessageNotification": {
        "Key": "f-1548",
        "Type": 8,
        "Message": "New message from Dr. Ben: <div>Thanks John</div>",
        "ObjectKey": "f562874"
    }
}
```
