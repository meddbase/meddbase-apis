---
layout: page
title: MembershipSchemeData
nav_order: 47
parent: Objects and data types
---

# MembershipSchemeDataProvides information about a membership scheme.## Properties| Name | string | Name of the scheme. || --- | --- | --- || Code | string | Membership code of the scheme. || BillingFrequency | string | Billing frequency of current scheme. Weekly, monthly, etc. || CurrencyCode | string | Three-letter currency code (e.g. "GBP", "EUR", "USD", etc.) || CurrencySymbol | string | Symbol for the currency || NetPrice | decimal |     || Tax | decimal |     || GrossPrice | decimal |     || RequiresOnlinePayment | bool | Scheme requires an online recurring payment method set up || OnlinePaymentAllowed | bool | The scheme allows online recurring payments. |## JSON Example```{"Name": "Basic Membership Program","Code": "ms001","BillingFrequency": "Monthly","CurrencyCode": "GBP","CurrencySymbol": "£","NetPrice": 100,"Tax": 20,"GrossPrice": 120,"RequiresOnlinePayment": false,"OnlinePaymentAllowed": true}```