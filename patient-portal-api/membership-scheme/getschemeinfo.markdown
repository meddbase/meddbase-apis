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

GET

## ****Url****

/patientportalapi/membership-scheme/scheme-info

## URL Parameters

| code | string | Membership scheme code that is provided by Medical Management Systems to the client. |
| --- | --- | --- |

## Returns

MembershipSchemeData
