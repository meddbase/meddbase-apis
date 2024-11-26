---
layout: page
title: TimeSlotsData
nav_order: 86
parent: Objects and data types
---

# TimeSlotsData

## Properties

| TimeSlots | [TimeSlotData](#_TimeSlotData)\[\] | The list of proposed time slots. |
| --- | --- | --- |
| Type | [AppointmentTypeData](#_AppointmentTypeData_1) | Appointment type of the proposed time slots. |
| Sites | [SiteData](#_SiteData)\[\] | The deduplicated list of sites for the found time slots, you can use the SiteKey in a TimeSlotData to find the relevant SiteData, and use the LocationKey to find the relevant LocationData inside the Locations inside a SiteData. Note that the Locations within each Site are only the locations that are relevant to found TimeSlots, not all Locations for the site. |
| Services | [ServiceData](#_PatientAbsenceData)\[\] | Services related to the appointment. |
| Modules | [AppointmentModuleData](#_AppointmentModuleData_1)\[\] | Modules related to the appointment. |
| Currency | [CurrencyData](#_CurrencyData) | The currency data that represents the currency for all prices in the returned time slots. |

## JSON Example

```
{

"TimeSlots": \[

{

"Start": "2025-01-01T09:30:00",

"Finish": "2025-01-01T10:30:00",

"SiteKey": 1123,

< See [TimeSlotData](#_TimeSlotData) to see all properties. >

},

{

"Start": "2025-01-01T10:30:00",

"Finish": "2025-01-01T11:30:00",

"SiteKey": 1123,

"LocationKey": 214,

< See [TimeSlotData](#_TimeSlotData) to see all properties. >

}

\],

"Type": {

"Key": "CN",

"Name": "Consultation"

},

"Sites": \[

{

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

},

"Locations": \[

{

"Key": 214,

"Name": "Room 1"

"Address": {

"Address1": "2 Clifton Park Ave",

"Address2": "",

"Address3": "",

"City": "London",

"County": "",

"PostCode": "SW20 8BD",

"Country": "United Kingdom"

}

}

\]

}

\],

"Services": \[

{

< See [ServiceData](#_PatientAbsenceData) to see all properties. >

},

{

< See [ServiceData](#_PatientAbsenceData) to see all properties. >

}

\],

"Modules": \[

{

< See [AppointmentModuleData](#_AppointmentModuleData_1) to see all properties. >

},

{

< See [AppointmentModuleData](#_AppointmentModuleData_1) to see all properties. >

}

\],

"Currency": {

"Code": "GBP",

"Symbol": "£"

}

}
```
