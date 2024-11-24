---
layout: page
title: Client authentication
nav_order: 4
parent: Communication overview
---

# Client authenticationThe client must provide the client’s identification key in every GET/POST request.The client identification key is provided by Medical Management Systems to the client. This key is a unique and can be built into the application code like a constant.The client identification key must be provided in a cookie with the key “Client-key”.Example:Client-key: a2gft68m-5d8b