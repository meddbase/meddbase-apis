---
layout: page
title: RecallData
nav_order: 74
parent: Objects and data types
---

# RecallDataProvides information about the recall.## Properties| Key | string | The key of the recall. || --- | --- | --- || Patient | PersonDemographicData | The patient data. || Reason | string | The reason for the recall. || AppointmentType | AppointmentTypeData | The appointment type. || DueDate | DateTime | Recall due date. || Clinician | ClinicianData | The clinician who triggered the recall. |## JSON Example```{"Key": "3bdd966cf6f9c0c6872ee0551da74c4d","DueDate": "2017-03-14T00:00:00","Reason": "Test","AppointmentType": {...},"Patient": {...},"Clinician": {...}}```