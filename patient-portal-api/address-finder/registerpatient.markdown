---
layout: page
title: RegisterPatient
nav_order: 3
parent: Address Finder
---

# RegisterPatient

Prepares a new registration. The patient is not fully created within the system until the appointment is booked.

## JavaScript library method

```javascript
patientportal.anonBooking.registerPatient({
    payerType: <payerType>,
    demog: <demog>
});
```

## HTTP Method

POST

## ****Url****

/patientportalapi/anon-booking/register-patient

## POST Parameters

<table><tbody><tr><th><p>payerType</p></th><th><p>String</p><p>(Optional)</p></th><th><p>The signup code of a chargeband, that will provide eligibility and price information for the search.</p><p>This is the same payer type like the one provided into the slot search GetProposedAppointments</p></th></tr><tr><td><p>demog</p></td><td><p>PersonDemographicData</p></td><td colspan="2"><p>Person demographics. Mandatory fields are:</p><ul><li>Name</li><li>Surname</li><li>EmailAddress</li><li>Mobile</li><li>DateOfBirth<ul><li>based on DateOfBirthRequiredForPatients in GetConfig</li></ul></li></ul></td></tr></tbody></table>

## Returned JSON

```
{

"SessionId": "R9I8Dr8rGQcQ6EOfxVyOBX2r8zt4KTO06vW0O2+GyFc="

}
```

## Remarks

A 2FA email and SMS message are automatically sent to the patient.
