---
layout: page
title: Direct Login
nav_order: 3
parent: Authentication
---

# Direct LoginAllows the client to authenticate their login using a unique token and to create the security context (session) with the Meddbase server.## JavaScript library methodpatientportal.auth.directLogin({loginToken: &lt;sslogin-token&gt;,});## HTTP MethodPOST## ****Url****/patientportalapi/auth/direct-login## URL Parameters| loginToken | guid | Unique login token. This token expires after 20 seconds of creation. || --- | --- | --- |## ReturnsAuthenticationData## RemarksThis is used for [Single Sign-on](#_Single_sign-on).If authentication is successful, a new session for the client is created and a new key ASP.NET_SessionId is added to the cookie. The client must ensure that this cookie will be sent in all further requests that needs to use the person’s security context.The SessionID can expire, so the client must use the ValidateLogin method to ensure that the security context is still created and the SessionID is still valid. If not, the client must login again.