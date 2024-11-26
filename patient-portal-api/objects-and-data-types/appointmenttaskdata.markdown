---
layout: page
title: AppointmentTaskData
nav_order: 10
parent: Objects and data types
---

# AppointmentTaskData

An additional details for the book/arrive appointment task.

## Properties

| AppointmentType | string | The type of the appointment that needs to be booked. |
| --- | --- | --- |
| AppointmentTypeName | string | The name of the appointment type.. |
| ServiceId | int | The optional service ID that needs to be included within the booking process. |
| IsBooked | bool | True if the appointment is already booked. |
| Clinician | string | The name of the clinician if the appointment is already booked. |
| StartDate | DateTime | The appointment start date if the appointment is already booked. |
| FinishDate | DateTime | The appointment finish date if the appointment is already booked. |
