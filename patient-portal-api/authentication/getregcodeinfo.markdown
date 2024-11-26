---
layout: page
title: GetRegCodeInfo
nav_order: 7
parent: Authentication
---

# GetRegCodeInfo

Returns information for the online sign-up access code (i.e. charge band information, because the online sign-up access code is assigned to the charge band).

## JavaScript library method

patientportal.auth.getRegCodeInfo({regCode: &lt;reg-code&gt;});

## HTTP Method

GET

## ****Url****

/patientportalapi/auth/reg-code-info

## URL Parameters

| reg-code | string | Online sign up access code that is provided to the patient. |
| --- | --- | --- |
| is-oh | bool | True for the referral portal. False for the patient portal. |

## Returns

ChargeBandData
