---
layout: page
title: SubmitValidationCode
nav_order: 3
parent: Anonymous Appointment Booking
---

# SubmitValidationCode

Submits the 2FA code and allows the booking process to continue.

## JavaScript library method

```javascript
patientportal.anonBooking.submitValidationCode({ code: <code> });
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/anon-booking/submit-validation-code` |

## POST Parameters

| code | code | The 2FA code. |
| --- | --- | --- |
