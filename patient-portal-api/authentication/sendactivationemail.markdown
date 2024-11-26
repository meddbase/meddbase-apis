---
layout: page
title: SendActivationEmail
nav_order: 11
parent: Authentication
---

# SendActivationEmail

Sends the activation email to the patient’s email address. The activation email includes a link to the patient portal website and contains the activation key: <https://www.yourportal.com/#/confirm-email?key=><key\>

## JavaScript library method

```javascript
patientportal.auth.sendActivationEmail({isOH: <is-oh>});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/auth/send-activation-email

## URL Parameters

| is-oh | bool | True for the referral portal. False for the patient portal. |
| --- | --- | --- |

## Remarks

Sometimes the patient needs to send the activation email again because (for example) she deletes it before activating her account or the last validation email was marked as a spam and it was deleted automatically.

The client needs to submit confirmation key from the URL by calling SubmitActivationEmail.

Remember the method needs the session ID to be set.
