---
layout: page
title: PatientRegistrationResultData
nav_order: 58
parent: Objects and data types
---

# PatientRegistrationResultData

Contains the details information about successful registration.

## Properties

<table><tbody><tr><th><p>ActivationType</p></th><th><p>int</p></th><th><p>How can the patient activate her account:</p><ul><li>1 = email activation</li><li>2 = SMS activation</li><li>3 = email or SMS activation</li></ul><p>The server choose activation type according actual configuration.</p><p>The client uses this information to provide right information about activation to the patient.</p></th></tr></tbody></table>

## JSON Example

```json
{
    "ActivationType": 2
}
```
