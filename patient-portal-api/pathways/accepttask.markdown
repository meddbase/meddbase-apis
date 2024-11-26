---
layout: page
title: AcceptTask
nav_order: 5
parent: Pathways
---

# AcceptTask

Accepts the general task within the pathway.

## JavaScript library method

```javascript
patientportal.pathways.getPathway({
    pathway: <pathway>,
    task: <task>
});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/pathways/accept-task

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| pathway | string | Pathway key |
| task | string | Task key |

## Returns

PathwayData
