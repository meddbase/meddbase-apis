---
layout: page
title: GetPayerTypes
nav_order: 1
parent: Appointments
---

# GetPayerTypes

Gets payer types (e.g. Patient, Employer, Issuer, School, etc.). This allows the patient to nominate another payer to pay for services.

## JavaScript library method

```javascript
patientportal.appointment.getPayerTypes({
    patient: <patient>,
    referral: <referral>,
    recall: <recall>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/appointment/payer-types` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| patient | string (optional) | The key of the patient provided by the API upon section Patients.<br><br>Used to book an appointment for a different patient within your company. Default is the logged in patient. |
| referral | string (optional) | The key of the referral provided by the API upon GetReferrals.<br><br>Used to book an appointment for a specific referral. |
| recall | string (optional) | The key of the recall provided by the API upon method GetRecalls.<br><br>Used to book an appointment for a specific recall. |

## Returns

[PayerType](../objects-and-data-types/payertype)[]

## Remarks

The method always returns at least one payer type. If there are more payer types the first type is patient’s default payer type.
