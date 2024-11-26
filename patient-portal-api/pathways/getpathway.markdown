---
layout: page
title: GetPathway
nav_order: 3
parent: Pathways
---

# GetPathway

Returns a specific pathway.

## JavaScript library method

```javascript
patientportal.pathways.getPathway({
    pathway: <pathway>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/pathways/pathway` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| pathway | int | Pathway ID |

## Returns

PathwayData
