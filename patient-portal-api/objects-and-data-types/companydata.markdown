---
layout: page
title: CompanyData
nav_order: 20
parent: Objects and data types
---

# CompanyData

Data returned in response to call to Insurers. Only companies marked as ‘Public’ are returned.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Key | string | Encrypted key of the company |
| Name | string | Public name of the company |
| Type | string | Type of the company: Insurer, etc. |
| IsPublic | bool | True: Only public companies are returned |

## JSON Example

```json
{
    "Key": "1c5aabbdf813ad78c48cc8e6d8584162",
    "Name": "Public Insurance",
    "Type": "Insurer",
    "IsPublic": true
}
```
