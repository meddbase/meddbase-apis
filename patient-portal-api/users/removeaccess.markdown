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

GET

## ****Url****

/patientportalapi/users/remove-access

## URL Parameters

| user | string | The key of the user provided by the API upon GetUsers. |
| --- | --- | --- |
