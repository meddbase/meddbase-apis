---
layout: page
title: LocalDateTime
nav_order: 42
parent: Objects and data types
---

# LocalDateTimeSame like DateTime but without information about a time zone. It is used for example to search for an appointment slot across time zones.Imagine this situation: the client is based in -6 zone but runs clinics also in both -7 and -6 zones. The patient is currently in -6 zone (or on holiday in -9 zone) and is looking for an appointment at 10am. For the patient 10am is local time and he expects slots in all three zones to start at 10am at site time.Required formatting: "yyyy-MM-ddTHH:mm:ss".## ExampleFebruary 2013, 13:2:25 = "2013-02-01T13:02:25"