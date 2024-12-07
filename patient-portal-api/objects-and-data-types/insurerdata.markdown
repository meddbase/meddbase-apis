---
layout: page
title: InsurerData
nav_order: 37
parent: Objects and data types
---

# InsurerData

Data returned in response to call to [Insurers](../companies/insurers). Only companies marked as ‘Public’ are returned.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Key | string | Encrypted key of the company |
| Name | string | Public name of the company (empty if company is private) |
| Type | string | Type of the company: Insurer, etc. |
| IsPublic | bool | Company is public or private |
| MemberNumber | string | Member number of the patient |

## JSON Example

```json
{
    "Key": "1c5aabbdf813ad78c48cc8e6d8584162",
    "Name": "Public Insurance",
    "Type": "Insurer",
    "IsPublic": true,
    "MemberNumber": "Test member number"
}
```
