---
layout: page
title: Single sign-on
nav_order: 27
parent: Patient Portal API
---

# Single sign-on
Meddbase system provides integration with SAML2 based single sign on providers.For identity provider initiated single sign on, the SAML request is sent to the API Gateway as a POST. The request is sent to following URL:<https://api.meddbase.com/ssoapi>The gateway generates a unique login token (uuid) and the user is redirected to the portal url configured in the application as follows:<https://portalurl/#/ssologin?loginToken=token>This token is valid for 20 seconds from the time of creation and is marked as expired after that time. The token can be used to login using [Direct Login](#_Direct_Login). Any error are passed as “error” query parameter.For service provider initiated single sign on calls, [SSO Login Details](#_Single_sign_on) call is used to retrieve the URL to redirect to the identity provider to login. The user is redirected to the provided URL, where once logged in, the identity provider sends a SAML response to the URL above, following the same workflow.