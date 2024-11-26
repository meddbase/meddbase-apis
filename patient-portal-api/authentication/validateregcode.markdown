---
layout: page
title: ValidateRegCode
nav_order: 6
parent: Authentication
---

# ValidateRegCode

Confirms the validity of the online sign up access code.

## JavaScript library method

patientportal.auth.validateRegCode({regCode: &lt;reg-code&gt;, isOH: &lt;is-oh&gt;});

## HTTP Method

GET

## ****Url****

/patientportalapi/auth/validate-reg-code

## URL Parameters

| reg-code | string | Online sign up access code that is provided to the patient. |
| --- | --- | --- |
| is-oh | bool | True for the referral portal. False for the patient portal. |

## Returns

ChargeBandData

## Remarks

If the registration code is invalid, check the exception (see Error handling).
