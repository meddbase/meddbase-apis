---
layout: page
title: Send2faCodeEmail/Send2faCodeSMS
nav_order: 28
parent: Authentication
---

# Send2faCodeEmail/Send2faCodeSMS

Sends generated 2FA code via specified method and returns delivery method.

## JavaScript library methods

```javascript
patientportal.auth.send2faCodeEmail();
    patientportal.auth.send2faCodeSMS();
```

## HTTP Method

POST

## Url

/patientportalapi/auth/send-2fa-code

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| useMobile | boolean | True to send 2FA code via mobile. False to send 2FA code via email. |

## Returned JSON

```
{

"DeliveryMethod": "Mobile"

}
```

## Remarks

Multiple methods are provided in the JavaScript library for ease of use.
