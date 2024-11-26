---
layout: page
title: SendPasswordResetEmail
nav_order: 19
parent: Authentication
---

# SendPasswordResetEmail
{: .d-inline-block }

Deprecated
{: .label .label-red }

{: .deprecated }
See [Password Reset](../password-reset/password-reset) section for more details.

If you still use this method please be aware that parameters name, surname and dateOfBirth are being ignored for a security reasons. The demographic details are validated within \[DEPRECATED\] SubmitPasswordResetEmail.

Disables patient’s account, sends a password reset request email that includes a URL address to the patient portal website that contains password reset key: <http://www.yourportal.com/#/password-reset?key=><key\>

## JavaScript library method

```javascript
patientportal.auth.sendPasswordResetEmail({
    'email': 'email',
    'name': 'name',
    'surname': 'surname',
    'dateOfBirth': 'date-of-birth',
    'isOH': true
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/auth/send-password-reset-email`|

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| is-oh     | bool   | True for the referral portal. False for the patient portal. |

## POST Parameters

| Parameter   | Type     | Description              |
|:------------|:---------|:-------------------------|
| email       | string   | Patient's email address. |
| name        | string   | Patient's name.          |
| surname     | string   | Patient's surname.       |
| dateOfBirth | DateTime | Patient's date of birth. |

{: .note }
> The server send an email with further instructions to the patient’s email address. The patient must follow those instructions to finish password reset process. The client should give the user advice that this email may be in their junk/spam folder.
> 
> The client needs to submit reset key from the URL and additional info from the patient by calling [SubmitPasswordResetEmail](submitpasswordresetemail).
