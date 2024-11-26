---
layout: page
title: ResetPassword
nav_order: 10
parent: Users
---

# ResetPassword

Resets user’s current password and sends an email request to reset password.

## JavaScript library method

```javascript
patientportal.users.resetPassword({
    user: <user>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/users/reset-password` |

## URL Parameters

| user | string | The key of the user provided by the API upon GetUsers. |
| --- | --- | --- |
