---
layout: page
title: AcceptTermsAndConditions
nav_order: 5
parent: Patient
---

# AcceptTermsAndConditions

Accepts both the Terms and conditions and the statistical processing of the patient data terms. The client needs to call GetTermsAndConditions to get texts of both. The patient have to accept both terms at once.

## JavaScript library method

```javascript
patientportal.patient.acceptTermsAndConditions({password: <password>});
```

## HTTP Method

POST

## ****Url****

/patientportalapi/patient/accept-terms-and-conditions

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| password | string | Patient’s plain text password to authenticate the patient. |
