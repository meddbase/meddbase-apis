---
layout: page
title: CreateUser
nav_order: 7
parent: Users
---

# CreateUser

Creates a new patient’s portal profile. If the patient already exists in the Meddbase system it joins the patient’s account with new portal profile.

## JavaScript library method

```javascript
patientportal.users.createUser({
    userData: <userData>
});
```

## HTTP Method

POST

## ****Url****

/patientportalapi/users/create-user

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| userData | UserData | Defines user’s details. |

## Returns

UserData

## Remarks

At least Name, Surname, DateOfBirth, EmailAddress, Mobile, Title, and Address.PostCode must be provided. Once the user is created she has the manager rights.

The Meddbase system sends the activation email with an activation link to the patient’s email address The user must activate her account first before being able to log-on. The client should give the user advice that the confirmation email may be in their junk/spam folder.

If the patient
