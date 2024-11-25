---
layout: page
title: SubmitPasswordResetEmail
nav_order: 20
parent: Authentication
---

# SubmitPasswordResetEmail
{: .d-inline-block }

Deprecated
{: .label .label-red }

{: .deprecated }
See [Password Reset](../password-reset/password-reset) section for more details.

Submit the password reset key that the client retrieves from the URL and additional information that the client collets from the patient.

## JavaScript Library

```javascript
patientportal.auth.submitPasswordResetEmail({
    key: 'key',
    name: 'name',
    surname: 'surname',
    dateOfBirth: 'date-of-birth',
    postcode: 'postcode',
    newPassword: 'new-password',
    isOH: true;
});
```

## HTTP Method

| Verb | URL                                                 |
|:-----|:----------------------------------------------------|
| POST | `/patientportalapi/auth/submit-password-reset-email`|

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| is-oh     | bool   | True for the referral portal. False for the patient portal. |


## POST Parameters

## POST Parameters

| Parameter   | Type     | Description                            |
|:------------|:---------|:---------------------------------------|
| key         | string   | Reset key that is included in the URL. |
| name        | string   | Patient's name.                        |
| surname     | string   | Patient's surname.                     |
| dateOfBirth | DateTime | Patient's date of birth.               |
| postcode    | string   | Patient’s address postcode.            |
| newPassword | string   | New password for patient's account.    |