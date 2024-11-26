---
layout: page
title: Send2faCode
nav_order: 27
parent: Authentication
---

# Send2faCode

Sends generated 2FA code via SMS or email and returns delivery method used.

## JavaScript library method

```
patientportal.auth.send2faCode();
```

## HTTP Method

GET

## Url

/patientportalapi/auth/send-2fa-code

## Returned JSON

```
{

"DeliveryMethod": "Mobile"

}
```

## Remarks

Code will be sent via SMS if the profile has a mobile number, otherwise it will be sent via email.
