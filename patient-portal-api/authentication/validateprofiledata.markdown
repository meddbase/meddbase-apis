---
layout: page
title: ValidateProfileData
nav_order: 9
parent: Authentication
---

# ValidateProfileData

Confirms the validity of the current patient’s demographic data.

## JavaScript library method

```javascript
patientportal.auth.validateProfileData({
    regCode: <regCode>,
    demog: <demog>,
    membershipCode: <membership-code>,
    isOH: <is-oh>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/auth/validate-profile-data` |

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| regCode | string (partially optional) | Online sign up access code that is provided to the patient. |
| demog | [PersonDemographicData](../objects-and-data-types/persondemographicdata) | Defines person’s details. |
| membershipCode | string (partially optional) | Membership scheme code that is provided by Medical Management Systems to the client.<br><br>See Membership scheme |
| is-oh | bool | True for the referral portal. False for the patient portal. |

## Remarks

One of the optional parameter regCode or membershipCode must be provided. If membership code is provided, regCode is ignored.

If the validation process is successful HTTP status code is 2xx. Otherwise check the exception (see Error handling).

Valid registration data:

- Name, Surname, DateOfBirth, EmailAddress, Mobile, Title, Address.PostCode and Password must be provided.
- Password should be at least 8 characters long and should contain at least 1 number.
