---
layout: page
title: GetUser
nav_order: 6
parent: Users
---

# GetUser

Returns the specific user.

## JavaScript library method

```javascript
patientportal.users.getUser({
    user: <user>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/users/user-data` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| user | string | The key of the user provided by the API upon GetUsers. |

## Returns

UserData
