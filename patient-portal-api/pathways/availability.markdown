---
layout: page
title: Availability
nav_order: 9
parent: Pathways
---

# AvailabilityReturns availability for a particular pathway definition if that pathways can be run by the patient.## JavaScript library method```patientportal.pathways.availability ({pathwayDef: &lt;pathwayDef&gt;}});```## HTTP MethodGET## ****Url****/patientportalapi/pathways/availability## URL Parameters| pathwayDef | string | Pathway Definition key || --- | --- | --- |## Returns[PathwayAvailabilityData](#_PathwayAvailabilityData)