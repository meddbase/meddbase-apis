---
layout: page
title: RegisterPatient
nav_order: 1
parent: Anonymous Appointment Booking
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

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/anon-booking/register-patient` |

## POST Parameters

<table>
    <thead>
        <tr>
            <th style="text-align: left">Parameter</th>
            <th style="text-align: left">Type</th>
            <th style="text-align: left">Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>payerType</td>
            <td>string (optional)</td>
            <td>
                <p>The signup code of a chargeband, that will provide eligibility and price information for the search.
                </p>
                <p>This is the same payer type like the one provided into the slot search GetProposedAppointments</p>
            </td>
        </tr>
        <tr>
            <td>demog</td>
            <td><a href="../objects-and-data-types/persondemographicdata">PersonDemographicData</a></td>
            <td>
                <p>Person demographics. Mandatory fields are:</p>
                <ul>
                    <li>Name</li>
                    <li>Surname</li>
                    <li>EmailAddress</li>
                    <li>Mobile</li>
                    <li>
                        DateOfBirth
                        <ul>
                            <li>based on DateOfBirthRequiredForPatients in GetConfig</li>
                        </ul>
                    </li>
                </ul>
            </td>
        </tr>
    </tbody>
</table>

## Returned JSON

```json
{
    "SessionId": "R9I8Dr8rGQcQ6EOfxVyOBX2r8zt4KTO06vW0O2+GyFc="
}
```

## Remarks

A 2FA email and SMS message are automatically sent to the patient.
