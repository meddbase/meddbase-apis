---
layout: page
title: ResendValidationCode
nav_order: 2
parent: Anonymous Appointment Booking
---

# ResendValidationCode

Resends the 2FA email and SMS. Please use the SessionId provide within registration and provide the ASP.NET_SessionId key in a cookie.

## JavaScript library method

```javascript
patientportal.anonBooking.resendValidationCode();
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/anon-booking/resend-validation-code` |
