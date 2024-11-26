---
layout: page
title: StartPathway
nav_order: 10
parent: Pathways
---

# StartPathway

Starts a pathway if allowed.

## JavaScript library method

```javascript
patientportal.pathways.startPathway({
    pathwayDef: <pathwayDef>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/pathways/start-pathway` |

## URL Parameters

| pathwayDef | string | Pathway Definition key |
| --- | --- | --- |

## Returns

Pathway Id (int)
