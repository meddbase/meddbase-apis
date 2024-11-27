---
layout: page
title: UpdateUser
nav_order: 8
parent: Users
---

# UpdateUser

Updates the user data.

## JavaScript library method

```javascript
patientportal.users.updateUser({
    userData: <userData>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/users/user-data` |

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| userData | [UserData](../objects-and-data-types/userdata) | Defines user’s details. |

## Returns

[UserData](../objects-and-data-types/userdata)
