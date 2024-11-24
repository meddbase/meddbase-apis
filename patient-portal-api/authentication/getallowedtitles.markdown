---
layout: page
title: GetAllowedTitles
nav_order: 8
parent: Authentication
---

# GetAllowedTitlesGets allowed titles (for example: Mr, Mrs, etc.) that can be used within registration process.## JavaScript library method```patientportal.auth.getAllowedTitles({regCode: &lt;reg-code&gt;,membershipCode: &lt;membership-code&gt;,isOH: &lt;is-oh&gt;});```## HTTP MethodGET## ****Url****/patientportalapi/auth/allowed-titles## URL Parameters| reg-code | string (optional) | Online sign up access code that is provided to the patient. || --- | --- | --- || membership-code | string (optional) | Membership scheme code that is provided by Medical Management Systems to the client.<br><br>See Membership scheme || is-oh | bool | True for the referral portal. False for the patient portal. |## Returnsstring\[\]## RemarksOne of the optional parameter reg-code or membership-code must be provided. If membership code is provided, registration code is ignored.