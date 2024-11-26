---
layout: page
title: GetSites
nav_order: 5
parent: Appointments
---

# GetSites

Gets possible sites for the specific appointment type. A site is a geographically-unique place. Each site may include additional 'locations', which are typically rooms at the site (Room 123, Surgery, etc.), but may also be geographically different places associated with the site (First floor, West wing, Building 3, etc.).

The API will only present you with locations which mean something to a user. So they're unlikely to get a choice about Room 1, 2, 3, etc. but they may get a choice about Site: My Bank, Location: Floor 1, Floor 50, Floor 100, etc.

## JavaScript library method

```javascript
patientportal.appointment.getSites({
    appointmentType: <appointment-type>,
    lat: <lat>,
    long: <long>,
    addressType: <address-type>,
    clinicians: <clinicians>,
    payerType: <payer-type>,
    patient: <patient>,
    referral: <referral>,
    recall: <recall>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/appointment/sites` |

## URL Parameters

<table><tbody><tr><th><p>appointment-type</p></th><th><p>string</p></th><th><p>Type of the appointment provided by the API upon GetAppointmentTypes.</p></th></tr><tr><td><p>lat</p><p>long</p></td><td><p>decimal (optional)</p></td><td><p>Latitude and Longitude from GPS so server can sort sites by distance.</p><p>Latitudes and Longitudes are defined using numerals that have a precision to 6 decimal places. For example, “lat=51.541743&amp;long=-0.13715" is a valid value.</p></td></tr><tr><td><p>address-type</p></td><td><p>int (optional)</p></td><td><p>Parameter specifies how the response should be sorted:</p><ul><li>1 = Home address</li><li>2 = Work address</li></ul><p>The server uses this value only if the GPS coordinate is not provided.</p></td></tr><tr><td><p>payer-type</p></td><td><p>string</p></td><td><p>Type of the payer provided by the API upon GetPayerTypes.</p></td></tr><tr><td><p>patient</p></td><td><p>string (optional)</p></td><td><p>The key of the patient provided by the API upon section Patients.</p><p>Used to book an appointment for a different patient within your company. Default is the logged in patient.</p></td></tr><tr><td><p>referral</p></td><td><p>string (optional)</p></td><td><p>The key of the referral provided by the API upon GetReferrals.</p><p>Used to book an appointment for a specific referral.</p></td></tr><tr><td><p>recall</p></td><td><p>string (optional)</p></td><td><p>The key of the recall provided by the API upon method GetRecalls.</p><p>Used to book an appointment for a specific recall.</p></td></tr></tbody></table>

## POST Parameters

| clinicians | int\[\] (optional) | Clinicians filter. Array of identifiers provide by the API upon GetClinicians. Null or empty for any clinicians. |
| --- | --- | --- |
| modules | [AppointmentModuleData](#_AppointmentModuleData) \[\] (optional) | Selection of modules and additional services provided by the API upon GetAppointmentTypes. Available sites will be filtered according to availability of the specified modules. |

## Returns

ShallowSearchResultData

A shallow search result of a patient/company address.

## Properties

| Key | string | An encrypted key value containing partial address information used to retrieve complete address details. |
| --- | --- | --- |
| Address | string | A single-line search result address. |

## JSON Example

```
{

"Key": "fc560b40315dc7605fd5ca53e0dcaabc357c69bea3faefa8c6e2ce8129909061956910b77338ee2c2cdbb1c7c5f7c64bcf338d78bc148f81f6786152d3ef2987b3ab5b1e5588b1db7939bb5e0edffec4614c4511c4a7a0dfd9bc9077749482b152217c572b0f78552c75be542ffcea6446110af6da78213c1f71569f35abab7d65f82f382f8b8dc663c8e6a1405bf17c331d379f375ffbc6ec3ebc21a985a69355d10622db48eceb7f23b38c5037ed2315c3d858268baae1879f6f84b3b65586742086832ec398acdfd56680a72991d7bb38bbfd1fa61991aebf0bd1982dc06b",

"Address": " 2 Paradise Street, Liverpool, Merseyside, L1 8JF"

}
```

###

SiteData\[\]

## Remarks

If no lat/long or addressType is provided the server sort sites by the patient’s home address.
