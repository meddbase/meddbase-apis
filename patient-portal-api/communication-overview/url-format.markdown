---
layout: page
title: URL format
nav_order: 1
parent: Communication overview
---

# URL format
All URL requests follow the following form:

`https://api.meddbase.com/patientportalapi/{section}/{method}?{param1}={value1}&{param2}={value2}&token={token}`

For example, the Login method of the Authentication section that requests two parameters: the 'username' and the 'password':

`https://api.meddbase.com/patientportalapi/auth/address-lookup?postcode=&postcode&house=house&token=token`

URL includes:

- section – A name of the section of the API that the method belongs to (e.g. 'auth', 'patient', 'finance', etc.). You can find the section name within the method description.
- method – A name of the method that the client wants to request (e.g. 'login', 'logout', etc.). You can find the method name within the method description.
- paramN, valueN – List of parameters. All parameters are separated using the ampersand (&) character. The list of parameters and their possible values are enumerated within the method description. Certain parameters are required while some are optional. Some methods do not require any parameters.
- token – A token provided by the API. See [Authentication Token](../authentication/authentication-token).
