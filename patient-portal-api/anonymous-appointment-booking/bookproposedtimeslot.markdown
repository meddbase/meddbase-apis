---
layout: page
title: BookProposedTimeSlot
nav_order: 5
parent: Anonymous Appointment Booking
---

# BookProposedTimeSlot

Creates the patient in our system and books an appointment from the time slot. Returns the new appointment.

## JavaScript library method

```javascript
patientportal.anonBooking.bookProposedTimeSlot({
    proposedTimeSlot: <proposeTimeSlot>,
    clinician: <clinician>,
    clinicianSex: <clinicianSex>,
    method: <method>,
    price: <price>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/anon-booking/book-time-slot` |

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
            <td>proposedTimeSlot</td>
            <td><a href="../objects-and-data-types/appointmentdata">AppointmentData</a></td>
            <td>The proposed time slot data, which can be constructed using the data provided by the <a href="#_GetProposedTimeSlots">GetProposedTimeSlots</a>.</td>
        </tr>
        <tr>
            <td>clinician</td>
            <td>int (optional)</td>
            <td>Clinician filter. Identifier provide by the API upon GetClinicians. Allow 0 for any clinician.</td>
        </tr>
        <tr>
            <td>clinicianSex</td>
            <td>int (optional)</td>
            <td>
                <p>Clinician’s gender filter:</p>
                <ul>
                    <li>0 = any sex</li>
                    <li>1 = male</li>
                    <li>2 = female</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>method</td>
            <td>int (optional)</td>
            <td>
                <p>The method that will be used to determine which slot to select if multiple are found that match the
                    given input criteria:</p>
                <ul>
                    <li>0 = random</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>price</td>
            <td>decimal (optional)</td>
            <td>Limit the bookable slots to only those that match the given price exactly</td>
        </tr>
    </tbody>
</table>

## POST data example

```json
{
    "proposedTimeSlot": {
        "Location": {
            "Key": 214
        },
        "Modules": [
            {
                "Key": 10382
            }
        ],
        "PayerType": "example",
        "Services": [],
        "Site": {
            "Key": 1123
        },
        "Start": "2025-01-01T09:30:00",
        "Type": {
            "Key": "00000000fc0af8e9"
        }
    },
    "clinicianSex": 1,
    "method": 0,
    "price": 100
}
```

## Returns

[AppointmentData](../objects-and-data-types/appointmentdata)

## Remarks

If no appropriate slot can be found for the proposed time slot, for example it was booked in the meantime, then an error is returned, see Error handling.
