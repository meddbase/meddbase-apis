---
layout: page
title: Logout
nav_order: 5
parent: Authentication
---

# LogoutCloses the security context.## JavaScript library methodpatientportal.auth.logout();## HTTP MethodGET## ****Url****/patientportalapi/auth/logout## RemarksIf the user is not logged in the exception is thrown (see Error handling).The client must provide the ASP.NET_SessionId key in the cookie.