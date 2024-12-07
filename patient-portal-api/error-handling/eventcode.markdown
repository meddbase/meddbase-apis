---
layout: page
title: EventCode
nav_order: 2
parent: Error handling
---

# EventCode

The client can use the EventCode property of the ServiceExceptionData object to identify the concrete type of the exception. Next table shows generally used codes but you can find another codes that can be thrown (these codes are described usually within Remarks section of the API methods).

| EventCode | Description       |
|:----------|:------------------|
| 0   | Not specified exception |
| 1   | Parameter is missing |
| 2   | Parameter has incorrect format (usually when integer contains letters or when date-time format is not valid) |
| 3   | Client authentication key is missing. |
| 4   | Client authentication key not valid. |
| 5   | Unknown API section (the sections means for example: finance, patient, auth, etc.) |
| 6   | Unknown API method. |
| 7   | Invalid or missing POST data. |
| 8   | User is not logged in. |
| 9   | Company name is missing. |
| 10  | Application is starting. Please wait and send the request later. |
| 11  | Invalid token. See [Authentication Token](../authentication/authentication-token). |
| 12  | Input includes HTML markup. |
| 13  | The client IP address is not in the allowed range specified in the employer settings. |
| 14  | User has been blocked because of too many failed login attempts. |
| 10001 | This account is already registered on our system as a private patient. |
| 40001 | Not all required questions of the questionnaire is answered. |
| 50001 | Medical history node you are looking for is not found. |
