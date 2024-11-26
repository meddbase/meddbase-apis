---
layout: page
title: GetBasicStatistics
nav_order: 12
parent: Referrals
---

# GetBasicStatistics

Returns the basic referral statistics.

## JavaScript library method

```javascript
patientportal.referrals.getBasicStatistics();
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/referrals/basic-statistics` |

## Returns JSON

```
\[

{

"Name": "In progress",

"Count": 21,

"Percent": 47

},

{

"Name": "Discharged",

"Count": 21,

"Percent": 53

}

\]
```
