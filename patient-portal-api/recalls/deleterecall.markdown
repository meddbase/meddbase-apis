---
layout: page
title: DeleteRecall
nav_order: 2
parent: Recalls
---

# DeleteRecall

Removes the recall.

## JavaScript library method

```javascript
patientportal.recalls.deleteRecall({
    recall: <recall>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/recall/delete` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| recall | string | The key of the recall provided by the API upon method [GetRecalls](../recalls/getrecalls). |
