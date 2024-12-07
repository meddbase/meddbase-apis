---
layout: page
title: PatientContactOption
nav_order: 57
parent: Objects and data types
---

# PatientContactOption

Contains the information about a permission the patient has given to the company to contact them on a specific subject by a specific way.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Key | string | The key of the contact option. This key is used to identify the contact option within [UpdateDemographicData](../patient/updatedemographicdata). |
| Subject | string | The name of subject. |
| Email | bool | Whether the patient has given a permission to contact them by email. |
| SMS | bool | Whether the patient has given a permission to contact them by a text message. |

## JSON Example

```json
{
    "Key": "Email.General",
    "Subject": "General human contact",
    "Email": true,
    "SMS": "true
}
```
