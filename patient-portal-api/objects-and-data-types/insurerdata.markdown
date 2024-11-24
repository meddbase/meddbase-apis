---
layout: page
title: InsurerData
nav_order: 37
parent: Objects and data types
---

# InsurerDataData returned in response to call to Insurers. Only companies marked as ‘Public’ are returned.## Properties| Key | string | Encrypted key of the company || --- | --- | --- || Name | string | Public name of the company (empty if company is private) || Type | String | Type of the company: Insurer, etc. || IsPublic | Bool | Company is public or private || MemberNumber | String | Member number of the patient |## JSON Example```{"Key": "1c5aabbdf813ad78c48cc8e6d8584162","Name": "Public Insurance","Type": "Insurer","IsPublic": true,"MemberNumber": "Test member number"}```