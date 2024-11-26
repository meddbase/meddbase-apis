---
layout: page
title: ApproveAndClose
nav_order: 6
parent: Absence Management
---

# ApproveAndCloseSets the status of the specified absence record to ‘closed’.## JavaScript library method```patientportal.absences.approveAndClose ({absence: &lt;absence&gt;});```## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/absences/approve-and-close` |## URL Parameters| absence | string | The key of the absence. || --- | --- | --- |## Returned JSON```{"status": "ok","result": {<[AbsenceData](#_AbsenceData)\>}}```