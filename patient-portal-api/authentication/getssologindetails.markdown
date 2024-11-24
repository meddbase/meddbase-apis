---
layout: page
title: GetSSOLoginDetails
nav_order: 26
parent: Authentication
---

# GetSSOLoginDetailsReturns unique URL to initiate a service provider initiated single sign on## JavaScript library method```patientportal.auth. getSSOLoginDetails ({companyIdentifier: &lt; company-identifier&gt;});```## HTTP MethodGET## ****Url****/patientportalapi/auth/sso-login-details## URL Parameters| company-identifier | string | Unique identifier to identify the employer’s single sign on configuration. || --- | --- | --- |## Returned JSONURL to be redirected to login through an identity provider## RemarksThis method is allowed only for the referral portal. Please see [Single sign on](#_Single_sign-on) for more details.