---
layout: page
title: BookProposedTimeSlot
nav_order: 7
parent: Address Finder
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

POST

## ****Url****

/patientportalapi/anon-booking/book-time-slot

## POST Parameters

<table><tbody><tr><th><p>proposedTimeSlot</p></th><th><p>AppointmentData</p></th><th><p>The proposed time slot data, which can be constructed using the data provided by the <a href="#_GetProposedTimeSlots">GetProposedTimeSlots</a>.</p></th></tr><tr><td><p>clinician</p></td><td><p>int (optional)</p></td><td><p>Clinician filter. Identifier provide by the API upon GetClinicians. Allow 0 for any clinician.</p></td></tr><tr><td><p>clinicianSex</p></td><td><p>int (optional)</p></td><td><p>Clinician’s gender filter:</p><ul><li>0 = any sex</li><li>1 = male</li><li>2 = female</li></ul></td></tr><tr><td><p>method</p></td><td><p>int (optional)</p></td><td><p>The method that will be used to determine which slot to select if multiple are found that match the given input criteria:</p><ul><li>0 = random</li></ul></td></tr><tr><td><p>price</p></td><td><p>decimal (optional)</p></td><td><p>Limit the bookable slots to only those that match the given price exactly</p></td></tr></tbody></table>

## POST data example

```
{

"proposedTimeSlot": {

"Location": {

"Key": 214

},

"Modules": \[

{

"Key": 10382

}

\],

"PayerType": "example",

"Services": \[\],

"Site": {

"Key": 1123

},

"Start":"2025-01-01T09:30:00",

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

AppointmentData

## Remarks

If no appropriate slot can be found for the proposed time slot, for example it was booked in the meantime, then an error is returned, see Error handling.
