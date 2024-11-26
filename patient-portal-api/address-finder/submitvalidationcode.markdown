---
layout: page
title: SubmitValidationCode
nav_order: 5
parent: Address Finder
---

# SubmitValidationCode

Submits the 2FA code and allows the booking process to continue.

## JavaScript library method

```javascript
patientportal.anonBooking.submitValidationCode({ code: <code> });
```

## HTTP Method

POST

## ****Url****

/patientportalapi/anon-booking/submit-validation-code

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| code | code | The 2FA code. |
