---
layout: page
title: GetServerState
nav_order: 21
parent: Authentication
---

# GetServerState

Returns information about actual server state.

## JavaScript library method

```javascript
patientportal.auth.getServerState();
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/auth/server-state` |

## Returns

[ServerStateData](../objects-and-data-types/serverstatedata)

## Remarks

This method doesn't require any authentication. The client can use this method to test connection to the server.
