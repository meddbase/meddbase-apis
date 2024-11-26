---
layout: page
title: GetDepartmentsAndDivisions
nav_order: 6
parent: Patient
---

# GetDepartmentsAndDivisions

Returns the list of employer departments and divisions.

## JavaScript library method

```javascript
patientportal.patient.getDepartmentsAndDivisions();
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/patient/departments-divisions` |

## Returned JSON

```
{

"Departments": \[

<list of DepartmentData>

\]

"Divisions": \[

<list of DivisionData>

\]

}
```
