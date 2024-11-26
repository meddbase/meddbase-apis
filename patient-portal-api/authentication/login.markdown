---
layout: page
title: Login
nav_order: 2
parent: Authentication
---

# Login

Allows the client to authenticate login credentials, initiate the 2FA process (if required) and create the security context (session) with the Meddbase server.

## JavaScript library method

```javascript
patientportal.auth.login({
    username: <username>,
    password: <password>,
    isOH: <is-oh>
});
```

## HTTP Method

POST

## ****Url****

/patientportalapi/auth/login

## URL Parameters

| is-oh | bool | True for the referral portal. False for the patient portal. |
| --- | --- | --- |

## POST Parameters

| username | string | Patient’s email address. |
| --- | --- | --- |
| password | string | Patient’s plain text password. |

## Returns

AuthenticationData

## Remarks

If authentication is successful, a new session for the client is created and a new key ASP.NET_SessionId is added to the cookie. The client must ensure that this cookie will be sent in all further requests that needs to use the person’s security context.

If 2FA is required, the profile will be marked as awaiting 2FA and will not be logged in. Once marked as awaiting 2FA, [Submit2faCode](#_Submit2faCode) must be completed successfully for the profile to be logged in.

The SessionID can expire, so the client must use the ValidateLogin method to ensure that the security context is still created and the SessionID is still valid. If not, the client must login again.
