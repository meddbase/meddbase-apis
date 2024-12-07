---
layout: page
title: GetSites
nav_order: 2
parent: Anonymous Appointment Search
---

# GetSites

Gets possible sites for the specific appointment type. A site is a geographically-unique place. Each site may include additional 'locations', which are typically rooms at the site (Room 123, Surgery, etc.), but may also be geographically different places associated with the site (First floor, West wing, Building 3, etc.).

The API will only present you with locations which mean something to a user. So they're unlikely to get a choice about Room 1, 2, 3, etc. but they may get a choice about Site: My Bank, Location: Floor 1, Floor 50, Floor 100, etc.

## JavaScript library method

```javascript
patientportal.anonAppointment.getSites({
    appointmentType: <appointment-type>,
    lat: <lat>,
    long: <long>,
    payerType: <payer-type>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/anon-appointment/sites` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| appointment-type | string | Type of the appointment provided by the API upon [GetAppointmentTypes](../anonymous-appointment-search/getappointmenttypes). |
| lat<br><br>long | decimal (optional) | Latitude and Longitude from GPS so server can sort sites by distance.<br><br>Latitudes and Longitudes are defined using numerals that have a precision to 6 decimal places. For example, “lat=51.541743&long=-0.13715" is a valid value. |
| payer-type | string | The signup code of a chargeband, that will provide eligibility and price information for the search. |

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| clinicians | int[] (optional) | Clinicians filter. Array of identifiers provide by the API upon <a href="../anonymous-appointment-search/getclinicians">GetClinicians</a>. Null or empty for any clinicians. |
| modules | [AppointmentModuleData](../objects-and-data-types/appointmentmoduledata)[] (optional) | Selection of modules and additional services provided by the API upon [GetAppointmentTypes](../anonymous-appointment-search/getappointmenttypes). Available sites will be filtered according to availability of the specified modules. |

## Returns

[SiteData](../objects-and-data-types/sitedata)[]
