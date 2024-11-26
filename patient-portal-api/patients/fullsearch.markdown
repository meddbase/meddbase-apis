---
layout: page
title: FullSearch
nav_order: 2
parent: Patients
---

# FullSearch

Returns the patient that meets the search criteria.

## JavaScript library method

```javascript
patientportal.patients.fullSearch({
    demog: <demog>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/patients/patient` |

## POST Parameters

| demog | PersonDemographicData | Defines person’s details. |
| --- | --- | --- |

## Returns

PersonDemographicData

## Remarks

The full search uses patient’s name, surname, email address, employee number, home address and data of birth to find the patient.

Throws various exceptions if there are duplicate records or if the user is not allowed to access the patient record.
