---
layout: page
title: GetSSOLoginDetails
nav_order: 26
parent: Authentication
---

# GetSSOLoginDetails

Returns unique URL to initiate a service provider initiated single sign on

## JavaScript library method

```javascript
patientportal.auth. getSSOLoginDetails({companyIdentifier: <company-identifier>});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/auth/sso-login-details` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| company-identifier | string | Unique identifier to identify the employer’s single sign on configuration. |

## Returned JSON

URL to be redirected to login through an identity provider

## Remarks

This method is allowed only for the referral portal. Please see [Single sign on](#_Single_sign-on) for more details.
