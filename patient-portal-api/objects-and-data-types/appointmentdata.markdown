---
layout: page
title: AppointmentData
nav_order: 7
parent: Objects and data types
---

# AppointmentData

Information about the appointment.

## Properties

<table><tbody><tr><th><p>Key</p></th><th><p>string</p></th><th><p>Key of the existing appointment.</p></th></tr><tr><td><p>Type</p></td><td><p>AppointmentTypeData</p></td><td><p>Type of appointment.</p></td></tr><tr><td><p>Start</p></td><td><p>DateTime</p></td><td><p>Start time.</p></td></tr><tr><td><p>Finish</p></td><td><p>DateTime</p></td><td><p>Finish time.</p></td></tr><tr><td><p>Site</p></td><td><p>ShallowSearchResultData</p><p>A shallow search result of a patient/company address.</p><h4>Properties</h4><table><tbody><tr><th><p>Key</p></th><th><p>string</p></th><th><p>An encrypted key value containing partial address information used to retrieve complete address details.</p></th></tr><tr><td><p>Address</p></td><td><p>string</p></td><td><p>A single-line search result address.</p></td></tr></tbody></table><h4>JSON Example</h4><p>{</p><p>"Key": "fc560b40315dc7605fd5ca53e0dcaabc357c69bea3faefa8c6e2ce8129909061956910b77338ee2c2cdbb1c7c5f7c64bcf338d78bc148f81f6786152d3ef2987b3ab5b1e5588b1db7939bb5e0edffec4614c4511c4a7a0dfd9bc9077749482b152217c572b0f78552c75be542ffcea6446110af6da78213c1f71569f35abab7d65f82f382f8b8dc663c8e6a1405bf17c331d379f375ffbc6ec3ebc21a985a69355d10622db48eceb7f23b38c5037ed2315c3d858268baae1879f6f84b3b65586742086832ec398acdfd56680a72991d7bb38bbfd1fa61991aebf0bd1982dc06b",</p><p>"Address": " 2 Paradise Street, Liverpool, Merseyside, L1 8JF"</p><p>}</p><h3><a id="_Toc182480988"></a></h3><p>SiteData</p></td><td><p>Where the appointment is placed.</p></td></tr><tr><td><p>Location</p></td><td><p>LocationData</p></td><td><p>Specific location within the site.</p></td></tr><tr><td><p>Patient</p></td><td><p>PersonDemographicData</p></td><td><p>The patient data.</p></td></tr><tr><td><p>Clinician</p></td><td><p>ClinicianData</p></td><td><p>Clinician of this appointment.</p></td></tr><tr><td><p>State</p></td><td><p>string</p></td><td><p>The state code of the appointment. Possible values:</p><ul><li>NotArrived</li><li>Cancelled</li><li>DNA</li><li>Discharged</li><li>BeingSeen</li><li>Arrived</li><li>Booked</li></ul></td></tr><tr><td><p>StateDisplayName</p></td><td><p>string</p></td><td><p>The friendly name of the appointment state.</p></td></tr><tr><td><p>StateColor</p></td><td><p>string</p></td><td><p>The preferred colour of the appointment state. Red for Cancelled and DNA. Otherwise green.</p></td></tr><tr><td><p>Modules</p></td><td><p>AppointmentModuleData[]</p></td><td><p>Modules related to the appointment.</p></td></tr><tr><td><p>Services</p></td><td><p>ServiceData<a href="../objects-and-data-types/servicedata">[]</a></p></td><td><p>Services related to the appointment</p></td></tr><tr><td><p>Slots</p></td><td><p>AppointmentSlot[]</p></td><td><p>List of appointment’s slots. Used for booking.</p></td></tr><tr><td><p>PrimaryAttendeeSlot</p></td><td><p>AppointmentSlot</p></td><td><p>Primary attendee slot. Used for booking.</p></td></tr><tr><td><p>Invoice</p></td><td><p>InvoiceData</p></td><td><p>Invoice related to this appointment. The client can provided information about payment status of the invoice and if the invoice is not paid the client can offer online payment.</p></td></tr><tr><td><p>Telemedicine</p></td><td><p>bool</p></td><td><p>Indicates whether the received appointment is telemedicine or not. On booking appointment the server ignores this parameter and books the appointment as telemedicine based on the <a href="#_Properties">TelemedicineOption</a> in AppointmentTypeData</p></td></tr><tr><td><p>TelemedicineConnection</p></td><td><p>string</p></td><td><p>URL for telemedicine connection to be launched in browser window. Whilst booking an appointment, this is left empty</p></td></tr><tr><td><p>AuthorisationCode</p></td><td><p>string</p></td><td><p>The authorisation code provided when the insurer is the payer.</p></td></tr></tbody></table>

## JSON Example

```
{

"Key": "apt58462",

"Type": {

"Key": "CN",

"Name": "Consultation",

},

"Start": "2013-08-07T09:30:00",

"Finish": "2013-08-07T10:30:00",

"Telemedicine": true,

"TelemedicineConnection": "<http://Meddbase.sandboxga.com/flex.html?roomdirect.html&key=Wchof474qrCO2QLrNK1SEMdrRY>",

"AuthorisationCode": "ABC123",

"Site": {

"Key": 1123,

"Name": "2CP (Eye Room)",

"Address":{

"Address1": "2 Clifton Park Ave",

"Address2": "",

"Address3": "",

"City": "London",

"County": "",

"PostCode": "SW20 8BD",

"Country": "United Kingdom"

}

}

"Location": {

"Key": 214,

"Name": "Room 1"

"Address":{

"Address1": "2 Clifton Park Ave",

"Address2": "",

"Address3": "",

"City": "London",

"County": "",

"PostCode": "SW20 8BD",

"Country": "United Kingdom"

}

},

"Clinician": {

"Key": 84,

"Name": "Dr. House"

},

"Slots": \[

{

< See _AppointmentSlot_ to see all properties. >

},

{

< See _AppointmentSlot_ to see all properties. >

}

\],

"PrimaryAttendeeSlot": {

< See _AppointmentSlot_ to see all properties. >

},

"Invoice": {

"Date": "2013-08-02",

"Number": "1865",

"NetPrice": 200,

"Vat": 40,

"GrossPrice": 240,

"Paid": 150,

"Creditor": {

"Name": "AXA PPP Healthcare",

< See _InvoiceData_ to see all properties. >

},

"Debtor": {

"Name": "Mr. John Lemon",

< See _InvoiceData_ to see all properties. >

}

}

}
```
