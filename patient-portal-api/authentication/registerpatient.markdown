---
layout: page
title: RegisterPatient
nav_order: 10
parent: Authentication
---

# RegisterPatient

Creates a new patient’s portal profile. If the patient already exists in the Meddbase system it joins the patient’s account with this portal profile.

## JavaScript library method

```javascript
patientportal.auth.registerPatient({
    regCode: <regCode>,
    demog: <demog>,
    membershipCode: <membership-code>,
    isOH: <is-oh>
});
```

## HTTP Method

POST

## ****Url****

/patientportalapi/auth/register-patient

## POST Parameters

| regCode | string (partially optional) | Online sign up access code that is provided to the patient. |
| --- | --- | --- |
| demog | PersonDemographicData | Defines person’s details. |
| membershipCode | string (partially optional) | Membership scheme code that is provided by Medical Management Systems to the client.<br><br>See Membership scheme |
| is-oh | bool | True for the referral portal. False for the patient portal. |

## Returns

PatientRegistrationResultData

## Remarks

One of the optional parameter regCode or membershipCode must be provided. If membership code is provided, regCode is ignored.

The client is responsible for making sure T&C is provided and accepted and the patient also accepts statistical processing of data.

If the registration process is successful, HTTP status code is 2xx. Otherwise check the exception (see Error handling). If the account already exists on our system the client gets exception where event code is 10001.

The Meddbase system sends the activation email with an activation link to the patient’s email address or it sends the activation SMS with an activation code to the patient’s mobile number or it sends both (use returned PatientRegistrationResultData to find out what activation is used). The user must activate her account first before being able to log-on. If the email activation is used the client should give the user advice that the confirmation email may be in their junk/spam folder.

The registration creates a standard session and the activation needs to pass a correct session ID within the request.

## POST data example

```
{

"regCode": "1234",

"demog": {

"Title": "Mr",

"Name": "John",

"Surname": "Lemon",

"DateOfBirth": "1958-08-02T00:00:00",

"EmailAddress": "<john.lemon@test.com>",

"Password": "jon4535lemon",

... <see PersonDemographicData for all properties>

}

}
```
