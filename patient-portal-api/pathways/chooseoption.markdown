---
layout: page
title: ChooseOption
nav_order: 6
parent: Pathways
---

# ChooseOption

Selects an option within the choice task.

## JavaScript library method

```javascript
patientportal.pathways.chooseOption({
    pathway: <pathway>,
    task: <task>,
    index: <index>
});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/pathways/choose-option

## URL Parameters

| pathway | string | Pathway key |
| --- | --- | --- |
| task | string | Task key |
| index | int | The index of the option. Note that he index starts from 1. |

## Returns

PathwayData
