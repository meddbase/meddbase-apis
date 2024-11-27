---
layout: page
title: Direct Login
nav_order: 3
parent: Authentication
---

# Direct Login

Allows the client to authenticate their login using a unique token and to create the security context (session) with the Meddbase server.

## JavaScript library method

```javascript
patientportal.auth.directLogin({loginToken: <sslogin-token>});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/auth/direct-login` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| loginToken | guid | Unique login token. This token expires after 20 seconds of creation. |

## Returns

[AuthenticationData](../objects-and-data-types/authenticationdata)

## Remarks

This is used for [Single Sign-on](#_Single_sign-on).

If authentication is successful, a new session for the client is created and a new key ASP.NET_SessionId is added to the cookie. The client must ensure that this cookie will be sent in all further requests that needs to use the person’s security context.

The SessionID can expire, so the client must use the ValidateLogin method to ensure that the security context is still created and the SessionID is still valid. If not, the client must login again.
