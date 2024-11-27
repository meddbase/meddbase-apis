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

## Returns

[DepartmentData](../objects-and-data-types/departmentdata)[]
[DivisionData](../objects-and-data-types/divisiondata)[]

## Returned JSON

```json
{
    "Departments": [
        {
            "Key": "D123",
            "Name": "HR"
        }
    ],
    "Divisions": [
        {
            "Key": "Dv123",
            "Name": "Division 123"
        }
    ]
}
```
