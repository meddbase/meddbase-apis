---
layout: page
title: Authentication Token
nav_order: 1
parent: Authentication
---

# Authentication Token

The authentication token needs to be included in every request sent to the API gateway while the user is logged-in. The token is a unique string generated for the current logged-in session. It changes on login/logout and expires together with the session if the session is not accessed for a lengthy period.

The only way to get the token is from the response of the [Login](../authentication/login) request and it is mandatory for all methods where the user is logged-in.

If the passed token is not valid, an Invalid Token exception (see [Error handling](../error-handling/error-handling)) is thrown.

One of the purposes of the token is to protect against the Cross-Site Request Forgery (CSRF).

Note that you do not need to manage the authentication token if you use our API Javascript library. It manages this for you automatically.
