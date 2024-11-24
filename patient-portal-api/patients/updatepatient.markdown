---
layout: page
title: UpdatePatient
nav_order: 6
parent: Patients
---

# UpdatePatientUpdates the patient demographic data.## JavaScript library method```patientportal.patients.updatePatient({demog: &lt;demog&gt;});```## HTTP MethodPOST## ****Url****/patientportalapi/patients/update-patient## POST Parameters| demog | PersonDemographicData | Defines person’s details. || --- | --- | --- |## ReturnsPersonDemographicData## RemarksThrows an exception if the patient doesn’t exist.