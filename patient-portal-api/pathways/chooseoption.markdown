---
layout: page
title: ChooseOption
nav_order: 6
parent: Pathways
---

# ChooseOption

Selects an option within the choice task.

## JavaScript library method

```
patientportal.pathways.chooseOption({

pathway: &lt;pathway&gt;,

task: &lt;task&gt;,

index: &lt;index&gt;

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
