---
layout: page
title: RemoveAccess
nav_order: 9
parent: Users
---

# RemoveAccess

Removes the manager’s rights so the user will not be able to access the Referral Portal sections.

## JavaScript library method

```javascript
patientportal.users.removeAccess({
    user: <user>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/users/remove-access` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| user | string | The key of the user provided by the API upon [GetUsers](../users/getusers). |
