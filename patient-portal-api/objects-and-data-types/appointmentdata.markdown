---
layout: page
title: AppointmentData
nav_order: 7
parent: Objects and data types
---

# AppointmentData

Information about the appointment.

## Properties

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
            <td>Key</td>
            <td>string</td>
            <td>Key of the existing appointment.</td>
        </tr>
        <tr>
            <td>Type</td>
            <td><a href="../objects-and-data-types/AppointmentTypeData">AppointmentTypeData</a></td>
            <td>Type of appointment.</td>
        </tr>
        <tr>
            <td>Start</td>
            <td><a href="../objects-and-data-types/DateTime">DateTime</a></td>
            <td>Start time.</td>
        </tr>
        <tr>
            <td>Finish</td>
            <td><a href="../objects-and-data-types/DateTime">DateTime</a></td>
            <td>Finish time.</td>
        </tr>
        <tr>
            <td>Site</td>
            <td><a href="../objects-and-data-types/sitedata">SiteData</a></td>
            <td>Where the appointment is placed.</td>
        </tr>
        <tr>
            <td>Location</td>
            <td><a href="../objects-and-data-types/locationdata">LocationData</a></td>
            <td>Specific location within the site.</td>
        </tr>
        <tr>
            <td>Patient</td>
            <td><a href="../objects-and-data-types/persondemographicdata">PersonDemographicData</a></td>
            <td>The patient data.</td>
        </tr>
        <tr>
            <td>Clinician</td>
            <td><a href="../objects-and-data-types/cliniciandata">ClinicianData</a></td>
            <td>Clinician of this appointment.</td>
        </tr>
        <tr>
            <td>State</td>
            <td>string</td>
            <td>
                <p>The state code of the appointment. Possible values:</p>
                <ul>
                    <li>NotArrived</li>
                    <li>Cancelled</li>
                    <li>DNA</li>
                    <li>Discharged</li>
                    <li>BeingSeen</li>
                    <li>Arrived</li>
                    <li>Booked</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>StateDisplayName</td>
            <td>string</td>
            <td>The friendly name of the appointment state.</td>
        </tr>
        <tr>
            <td>StateColor</td>
            <td>string</td>
            <td>The preferred colour of the appointment state. Red for Cancelled and DNA. Otherwise green.</td>
        </tr>
        <tr>
            <td>Modules</td>
            <td><a href="../objects-and-data-types/appointmentmoduledata">AppointmentModuleData</a>[]</td>
            <td>Modules related to the appointment.</td>
        </tr>
        <tr>
            <td>Services</td>
            <td><a href="../objects-and-data-types/servicedata">ServiceData</a>[]</td>
            <td>Services related to the appointment</td>
        </tr>
        <tr>
            <td>Slots</td>
            <td><a href="../objects-and-data-types/appointmentslot">AppointmentSlot</a>[]</td>
            <td>List of appointment’s slots. Used for booking.</td>
        </tr>
        <tr>
            <td>PrimaryAttendeeSlot</td>
            <td><a href="../objects-and-data-types/appointmentslot">AppointmentSlot</a></td>
            <td>Primary attendee slot. Used for booking.</td>
        </tr>
        <tr>
            <td>Invoice</td>
            <td><a href="../objects-and-data-types/invoicedata">InvoiceData</a></td>
            <td>
                <p>Invoice related to this appointment. The client can provided information about payment status of the
                    invoice and if the invoice is not paid the client can offer online payment.</p>
            </td>
        </tr>
        <tr>
            <td>Telemedicine</td>
            <td>bool</td>
            <td>
                <p>Indicates whether the received appointment is telemedicine or not. On booking appointment the server
                    ignores this parameter and books the appointment as telemedicine based on the <a
                        href="#_Properties">TelemedicineOption</a> in AppointmentTypeData</p>
            </td>
        </tr>
        <tr>
            <td>TelemedicineConnection</td>
            <td>string</td>
            <td>
                <p>URL for telemedicine connection to be launched in browser window. Whilst booking an appointment, this
                    is left empty</p>
            </td>
        </tr>
        <tr>
            <td>AuthorisationCode</td>
            <td>string</td>
            <td>The authorisation code provided when the insurer is the payer.</td>
        </tr>
    </tbody>
</table>

## JSON Example

```json
{
    "Key": "apt58462",
    "Type": {
        "Key": "CN",
        "Name": "Consultation"
    },
    "Start": "2013-08-07T09:30:00",
    "Finish": "2013-08-07T10:30:00",
    "Telemedicine": true,
    "TelemedicineConnection": "http://Meddbase.sandboxga.com/flex.html?roomdirect.html&key=Wchof474qrCO2QLrNK1SEMdrRY",
    "AuthorisationCode": "ABC123",
    "Site": {
        "Key": 1123,
        "Name": "2CP (Eye Room)",
        "Address": {
            "Address1": "2 Clifton Park Ave",
            "Address2": "",
            "Address3": "",
            "City": "London",
            "County": "",
            "PostCode": "SW20 8BD",
            "Country": "United Kingdom"
        }
    },
    "Location": {
        "Key": 214,
        "Name": "Room 1",
        "Address": {
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
    "Slots": [
        {
            "Type": "CN",
            "Start": "2013-08-07T09:30:00",
            "Finish": "2013-08-07T10:30:00",
            "SiteKey": 1123,
            "LocationKey": 214,
            "ResourceKey": 468
        }
    ],
    "PrimaryAttendeeSlot": {
        "Type": "CN",
        "Start": "2013-08-07T09:30:00",
        "Finish": "2013-08-07T10:30:00",
        "SiteKey": 1123,
        "LocationKey": 214,
        "ResourceKey": 468
    },
    "Invoice": {
        "Key": "inv4645",
        "Date": "2013-02-06",
        "Number": "1865",
        "CurrencyCode": "GBP",
        "CurrencySymbol": "£",
        "TotalNet": 200,
        "Tax": 40,
        "TotalGross": 240,
        "Paid": 150,
        "Creditor": {
            "Name": "AXA PPP Healthcare",
            "IsCompany": true,
            "Address": {
                "Address1": "44 Pall Mall",
                "City": "London",
                "PostCode": "SW1Y",
                "Country": "United Kingdom"
            },
            "Account": {
                "CODE": "AXA",
                "Name": "AXA PPP Healthcare",
                "Address": {
                    "Address1": "44 Pall Mall",
                    "City": "London",
                    "PostCode": "SW1Y",
                    "Country": "United Kingdom"
                }
            }
        },
        "Debtor": {
            "Name": "Mr. John Lemon",
            "IsCompany": false,
            "Address": {
                "Address1": "Studio 99",
                "Address2": "Backlok Street",
                "Address3": "Camden",
                "City": "London",
                "County": "",
                "PostCode": "N1 7NK",
                "Country": "United Kingdom"
            },
            "Account": {
                "Title": "Mr",
                "Name": "John",
                "Surname": "Lemon",
                "SexType": 1,
                "Initials": "JL",
                "DateOfBirth": "1958-08-02T00:00:00",
                "Mobile": "+444 895 523 411",
                "Telephone": "+444 525 111 555",
                "EmailAddress": "<john.lemon@test.com>",
                "Address": {
                    "Address1": "Studio 99",
                    "Address2": "Backlok Street",
                    "Address3": "Camden",
                    "City": "London",
                    "County": "",
                    "PostCode": "N1 7NK",
                    "Country": "United Kingdom"
                }
            }
        },
        "PayableOnline": true
    }
}
```
