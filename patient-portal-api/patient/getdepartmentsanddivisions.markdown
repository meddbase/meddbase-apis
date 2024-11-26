---
layout: page
title: GetDepartmentsAndDivisions
nav_order: 6
parent: Patient
---

# GetDepartmentsAndDivisions

Returns the list of employer departments and divisions.

## JavaScript library method

```
patientportal.patient.getDepartmentsAndDivisions();
```

## HTTP Method

GET

## ****Url****

/patientportalapi/patient/departments-divisions

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
