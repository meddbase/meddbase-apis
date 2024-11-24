---
layout: page
title: BulkReallocate
nav_order: 10
parent: Referrals
---

# BulkReallocateRe-allocate all referrals created by one user to a different user. Returns count of reallocated referrals.## JavaScript library method```patientportal.referrals.bulkReallocate({fromUser: &lt;from-user&gt;,patient: &lt;patient&gt;,toUser: &lt;to-user&gt;});```## HTTP MethodGET## ****Url****/patientportalapi/referrals/bulk-reallocate## URL Parameters| from-user | string (optional\*) | The key of the user provided by the API upon FindUserToReallocate. Use this filter to reallocate referrals assigned to a specific user. || --- | --- | --- || patient | string (optional\*) | The key of the patient provided by the API upon section Patients. Use this filter to reallocated referrals of a specific patient. || to-user | string | The key of the user provided by the API upon FindUserToReallocate. |## Remarks\* Either from-user or patient parameter must be provided.## Returned JSON```{"Referrals": 18}```