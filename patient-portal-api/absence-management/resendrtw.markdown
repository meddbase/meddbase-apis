---
layout: page
title: ResendRTW
nav_order: 5
parent: Absence Management
---

# ResendRTWResends the questionnaire request email / SMS for the specified absence record to the patient. Sets the absence record’s questionnaire status to ‘sent’ if not already set.## JavaScript library method```patientportal.absences.resendRTW ({absence: &lt;absence&gt;});```## HTTP MethodGET## ****Url****/patientportalapi/absences/resend-rtw## URL Parameters| absence | string | The key of the absence. || --- | --- | --- |## Returned JSON```{"status": "ok","result": {<[AbsenceData](#_AbsenceData)\>}}```