---
layout: page
title: AuthorizeTelemedicineData
nav_order: 14
parent: Objects and data types
---

# AuthorizeTelemedicineData

Returns authorisation data for a telemedicine connection.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Token | string | Secure token generated for the user joining the telemedicine conference. |
| Version | int | A version of the telemedicine integration. Currently always version 3 which means Twilio. |

## JSON Example

```
{

"Version": "3",

"Token": "ZS1Q8LUazO3Q2fRI...",

}
```
