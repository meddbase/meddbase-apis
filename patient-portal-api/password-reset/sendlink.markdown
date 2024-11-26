---
layout: page
title: SendLink
nav_order: 1
parent: Password reset
---

# SendLink

Sends a password reset link via an email to the patient’s personal email address or to the manager’s work email address. The link includes the portal URL with a password reset key in a format: <http://www.yourportal.com/#/password-reset?key=><key\>

## JavaScript library method

```javascript
patientportal.passwordReset.sendLink({ email: <email> });
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/password-reset/send-link` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| is-oh | bool | True for the referral portal. False for the patient portal. |

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| email | string | Email address. |

## Remarks

The email is sent even if the email address isn’t registered with us. In that case we inform user the email address is incorrect and we recommend them to try again or register.
