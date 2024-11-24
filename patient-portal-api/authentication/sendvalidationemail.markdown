---
layout: page
title: SendValidationEmail
nav_order: 15
parent: Authentication
---

# SendValidationEmail
{: .d-inline-block }

Deprecated
{: .label .label-red }

{: .deprecated }
Replaced with [SendActivationEmail](SendActivationEmail)

Sends the validation email to the patient’s email address. Validation email includes URL to the patient portal website and contains validation key: `http://www.yourportal.com/#/confirm-email?key={key}`

## JavaScript Library

```javascript
patientportal.auth.sendValidationEmail({
        email: 'email', 
        isOH: true
    });
```

## HTTP Method

| Verb | URL                                           |
|:-----|:----------------------------------------------|
| GET  | `/patientportalapi/auth/send-validation-email`|


### URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| email     | string | Patient’s email address.                                    |
| is-oh     | bool   | True for the referral portal. False for the patient portal. |


{: .note }
> Sometimes the patient needs to send the validation email again because (for example) she deletes it before activating her account or the last validation email was marked as a spam and it was deleted automatically.
> 
> The client needs to submit confirmation key from the URL by calling [SubmitValidationEmail](SubmitValidationEmail).
