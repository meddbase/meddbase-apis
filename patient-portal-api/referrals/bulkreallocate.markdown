---
layout: page
title: BulkReallocate
nav_order: 10
parent: Referrals
---

# BulkReallocate

Re-allocate all referrals created by one user to a different user. Returns count of reallocated referrals.

## JavaScript library method

```javascript
patientportal.referrals.bulkReallocate({
    fromUser: <from-user>,
    patient: <patient>,
    toUser: <to-user>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/referrals/bulk-reallocate` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| from-user | string (optional\*) | The key of the user provided by the API upon FindUserToReallocate. Use this filter to reallocate referrals assigned to a specific user. |
| patient | string (optional\*) | The key of the patient provided by the API upon section Patients. Use this filter to reallocated referrals of a specific patient. |
| to-user | string | The key of the user provided by the API upon FindUserToReallocate. |

## Remarks

\* Either `from-user` or `patient` parameter must be provided.

## Returned JSON

```json
{
    "Referrals": 18
}
```
