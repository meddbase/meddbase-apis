---
layout: page
title: GetDepartmentsAndDivisions
nav_order: 2
parent: Users
---

# GetDepartmentsAndDivisions

Returns the list of employer departments and divisions.

## JavaScript library method

```javascript
patientportal.users.getDepartmentsAndDivisions();
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/users/departments-divisions` |

## Returned JSON

```
{

"Departments": \[

&lt;list of DepartmentData&gt;

\]

"Divisions": \[

&lt;list of DivisionData&gt;

\]

}
```
