---
layout: page
title: Ethnicities
nav_order: 32
parent: Patient Portal API
---

# Ethnicities



Returns a list of the available ethnicities to select from when updating the patient’s details.

## JavaScript library method

```javascript
patientportal.ethnicities.getEthnicities();
```

## HTTP Method

GET

## ****Url****

/patientportalapi/ethnicities/ethnicities

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Key | string | The absence key. |

## Returns

[EthnicityData\[\]](#_EthnicityData)
