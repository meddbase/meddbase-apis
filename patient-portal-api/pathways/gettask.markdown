---
layout: page
title: GetTask
nav_order: 4
parent: Pathways
---

# GetTask

Returns a full task description.

## JavaScript library method

```javascript
patientportal.pathways.getTask({
    pathway: <pathway>,
    task: <task>
});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/pathways/task

## URL Parameters

| pathway | string | Pathway key |
| --- | --- | --- |
| task | string | Task key |

## Returns

PathwayTaskData
