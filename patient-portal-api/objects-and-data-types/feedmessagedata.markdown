---
layout: page
title: FeedMessageData
nav_order: 35
parent: Objects and data types
---

# FeedMessageData

One message in the message feed.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| AuthorName | string | Name of the author of this message. |
| Date | [DateTime](../objects-and-data-types/datetime) | Date when the message was created. |
| Text | string | Text of the message. HTML or plain text. |

## JSON Example

```json
{
    "AuthorName": "Dr. Ben",
    "Date": "2013-08-02T14:45:58.9525711+01:00",
    "Text": "<div><b>Hi John</b></div>"
}
```
