---
layout: page
title: SaveAbsence
nav_order: 3
parent: Absence Management
---

# SaveAbsenceSaves changes to an absence record. Any of the attributes in the [AbsenceData](#_AbsenceData) object can be modified and sent back to the API, but the only ones for which changes will be saved to the database are:- EndDate- LostWork.Days- LostWork.Hours- AccidentAtWork## JavaScript library method```patientportal.absences.saveAbsence({absenceData: &lt;absence-data&gt;});```## HTTP MethodPOST## ****Url****/patientportalapi/absences/absence## URL Parameters| absence-data | [AbsenceData](#_AbsenceData) | The [AbsenceData](#_AbsenceData) object received from a call to the [GetAbsence](#_GetAbsence) method. || --- | --- | --- |## Returned JSON```{"status": "ok","result": {<[AbsenceData](#_AbsenceData)\>}}```