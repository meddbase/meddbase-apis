---
layout: page
title: FullSearchOrCreate
nav_order: 3
parent: Patients
---

# FullSearchOrCreate

Returns the patient that meets the search criteria. If such as patient doesn’t exist then creates a new one.

## JavaScript library method

```javascript
patientportal.patients.fullSearchOrCreate({
    demog: <demog>
});
```

## HTTP Method

POST

## ****Url****

/patientportalapi/patients/create-patient

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| demog | PersonDemographicData | Defines person’s details. |

## Returns

PersonDemographicData

## Remarks

The full search uses patient’s name, surname, email address, employee number, home address and data of birth to find the patient.

If the patient doesn’t exist then the API creates a new patient.

Throws various exceptions if there are duplicate records or if the user is not allowed to access the patient record.
