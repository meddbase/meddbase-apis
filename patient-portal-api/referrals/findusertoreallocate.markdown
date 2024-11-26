---
layout: page
title: FindUserToReallocate
nav_order: 8
parent: Referrals
---

# FindUserToReallocate

Search for user to re-allocate the referral. The search provides only basic user’s data: Key, Name, Surname, EmployeeNumber and Title.

## JavaScript library method

```javascript
patientportal.referrals.findUserToReallocate({
    employeeNumber: <employee-number>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/referrals/find-user-to-reallocate` |

## URL Parameters

| employee-number | string | The user’s employee number. |
| --- | --- | --- |

## Returned JSON

```
{

"Key": "u1324",

"Title": "Mr."

"Name": "John",

"Surname": "Smith",

"EmployeeNumber": "1234"

}
```
