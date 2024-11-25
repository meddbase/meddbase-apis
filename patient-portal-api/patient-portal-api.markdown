---
layout: page
title: Patient Portal API
nav_order: 2
---

## Patient Portal API
The Meddbase Patient Portal API is a collection of endpoints intended for use in a patient centric context, direct from a browser. The supported use case for these API's is building patient centric workflows such as Patient Portals, Occupational Health Portals, and other related booking applications.

This is not intended for use as a system to system integration API. Any such integrations should be achieved using the Meddbase Enterprise API, and any questions regarding this functionality should, for now, be directed to your Meddbase Account Manager or Client Success Manager.

Most Patient Portal API endpoints require an authenticated Patient to utilise. This could either be a Patient making bookings or viewing data about themselves, or a manager performing actions for a patient they have authority to view/access.

Anonymous booking endpoints are also available, and can be used in circumstances when the patient's identity is not known at the time when the booking is initiated. 