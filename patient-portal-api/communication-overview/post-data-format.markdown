---
layout: page
title: POST data format
nav_order: 2
parent: Communication overview
---

# POST data formatCertain methods use the HTTP POST method to send data to the server. The client must format all POST data into the JSON format.For example, the method ValidateProfileData requires two POST parameters: the ‘regCode’ and the ‘demog’. The POST data example:```{"regCode": "&lt; value &gt;""demog": {&lt; properties &gt;}}```