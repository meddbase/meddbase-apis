---
layout: page
title: ChargeBandData
nav_order: 17
parent: Objects and data types
---

# ChargeBandDataProvides information about a chargeband.## Properties| Name | string | Name of the chargeband. || --- | --- | --- || RegCode | string | Online signup code of the chargeband. || CompanyType | string | Type of the company to which the signup code belongs || ProvideDeptsAndDivs (Optional) | bool | Flag that shows if registering person is allowed to see and select department and division. The value is only returned in patient portal. |## JSON Example```{"Name": "Online chargeband","RegCode": "d01m","CompanyType" : "M"}```