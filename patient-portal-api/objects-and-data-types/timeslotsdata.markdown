---
layout: page
title: TimeSlotsData
nav_order: 86
parent: Objects and data types
---

# TimeSlotsData

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| TimeSlots | [TimeSlotData](../objects-and-data-types/timeslotdata)[] | The list of proposed time slots. |
| Type | [AppointmentTypeData](../objects-and-data-types/appointmenttypedata) | Appointment type of the proposed time slots. |
| Sites | [SiteData](../objects-and-data-types/sitedata)[] | The deduplicated list of sites for the found time slots, you can use the SiteKey in a TimeSlotData to find the relevant SiteData, and use the LocationKey to find the relevant LocationData inside the Locations inside a SiteData. Note that the Locations within each Site are only the locations that are relevant to found TimeSlots, not all Locations for the site. |
| Services | [ServiceData](../objects-and-data-types/patientabsencedata)[] | Services related to the appointment. |
| Modules | [AppointmentModuleData](../objects-and-data-types/appointmentmoduledata)[] | Modules related to the appointment. |
| Currency | [CurrencyData](../objects-and-data-types/currencydata) | The currency data that represents the currency for all prices in the returned time slots. |

## JSON Example

```json
{
    "TimeSlots": [
        {
            "Start": "2025-01-01T09:30:00",
            "Finish": "2025-01-01T10:30:00",
            "SiteKey": 123,
            "LocationKey": 546,
            "GrossPrice": 240,
            "NetPrice": 200
        },
        {
            "Start": "2025-01-01T10:30:00",
            "Finish": "2025-01-01T11:30:00",
            "SiteKey": 123,
            "LocationKey": 546,
            "GrossPrice": 240,
            "NetPrice": 200
        }
    ],
    "Type": {
        "Key": "CN",
        "Name": "Consultation"
    },
    "Sites": [
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
            "Locations": [
                {
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
                }
            ]
        }
    ],
    "Services": [
        {
            "Code": "A1250",
            "CurrencyCode": "GBP",
            "CurrencySymbol": "£",
            "GrossPrice": 0,
            "Key": 593,
            "Name": "Creation of subcutaneous cerebrospinal fluid reservoir",
            "NetPrice": 0,
            "Tax": 0,
            "ServiceType": {
                "Key": 84,
                "Name": "Blood profile"
            }
        }
    ],
    "Modules": [
        {
            "Key": 5631,
            "Name": "Short Consult",
            "CurrencyCode": "GBP",
            "CurrencySymbol": "£",
            "NetPrice": 50,
            "Tax": 10,
            "GrossPrice": 60
        }
    ],
    "Currency": {
        "Code": "GBP",
        "Symbol": "£"
    }
}
```
