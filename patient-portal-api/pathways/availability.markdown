---
layout: page
title: Availability
nav_order: 9
parent: Pathways
---

# Availability

Returns availability for a particular pathway definition if that pathways can be run by the patient.

## JavaScript library method

```javascript
patientportal.pathways.availability({
    pathwayDef: <pathwayDef>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/pathways/availability` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| pathwayDef | string | Pathway Definition key |

## Returns

[PathwayAvailabilityData](../objects-and-data-types/pathwayavailabilitydata)
