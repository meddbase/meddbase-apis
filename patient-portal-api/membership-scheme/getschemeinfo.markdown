---
layout: page
title: GetSchemeInfo
nav_order: 2
parent: Membership scheme
---

# GetSchemeInfo

Returns information for the membership scheme (name, billing frequency, price, etc.).

## JavaScript library method

```javascript
patientportal.membershipScheme.getSchemeInfo({code: <code>});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/membership-scheme/scheme-info` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| code | string | Membership scheme code that is provided by Medical Management Systems to the client. |

## Returns

MembershipSchemeData
