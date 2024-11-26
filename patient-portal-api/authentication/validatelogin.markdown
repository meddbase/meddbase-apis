---
layout: page
title: ValidateLogin
nav_order: 4
parent: Authentication
---

# ValidateLogin

Confirms the validity of the current security context. Returns the current validation token and RemainingTime - the number of seconds for the session to stay active without any further request. Note that calling validateLogin does keep the session active.

## JavaScript library method

```javascript
patientportal.auth.validateLogin();
```

## HTTP Method

GET

## ****Url****

/patientportalapi/auth/validate

## Returned JSON

```
{

"Token": "380da8b1-d4ca-4d92-98d2-bbe3ce258a49",

"RemainingTime": 569

}
```

## Remarks

If the actual security context is valid, HTTP status code is 2xx. Otherwise check the exception (see Error handling) and use Login to create a new security context.

The client must provide the ASP.NET_SessionId key in the cookie.
