---
layout: page
title: Client authentication
nav_order: 4
parent: Communication overview
---

# Client authentication

To authenticate your requests, you must always provide an API client key and additionally where a logged in user context is required a session identifier.

## Client key

The client key must be provided with every request and can be provided in two ways:

- URL query parameter `client-key`
- Cookie named `Client-key`

Example using the `client-key` URL query parameter:

```
curl --request GET --url "https://api.meddbase.com/patientportalapi/auth/config?client-key=my-client-key"
```

Example using the `Client-key` cookie:

```
curl --request GET --url "https://api.meddbase.com/patientportalapi/auth/config" --header "Cookie: Client-key=my-client-key"
```

## Session identifier

Where a logged in user context is required, a session identifier must be sent with your requests. The login endpoint returns a session identifier in the response body. This session identifier can be used in subsequent requests by including it in the `x-session-id` header.

Example login request:

```
curl -X POST -H 'Content-Type: application/json' -d '{"username": "john.doe@example.com", "password": "MyPassword"}' --url "https://api.meddbase.com/patientportalapi/auth/login?client-key=my-client-key"
```

Example response JSON:

```
{
    "status": "ok",
    "result": {
        "SessionID": "my-session-id",
        "Token": "my-csrf-token"
    }
}
```

Using the `SessionID` and `Token` from the response, we can then send a request to an endpoint requiring the newly logged in session:

```
curl --request GET --url "https://api.meddbase.com/patientportalapi/appointment/existing-appointments?client-key=my-client-key" --header "x-session-id: my-session-id" --header "x-token: my-csrf-token"
```

{: .warning }
Sending the session identifier via POST body value `SessionId` or using a cookie `ASP.NET_SessionId` is still supported but now deprecated. The recommended method is to use the `x-session-id` header.

## CSRF tokens

Some endpoints will return a CSRF token as part of their response payload. Where present, this token must be included in your response to the server. This token should be sent in the `x-token` header.

{: .warning }
Sending the CSRF token via POST body value `Token` or using a `token` URL query parameter is still supported but now deprecated. The recommended method is to use the `x-token` header.
