---
layout: page
title: GetInsurer
nav_order: 8
parent: Patient
---

# GetInsurerGets a patient’s insurer. Only available for patient portal. Only public companies have details returned like Name, otherwise the returned object only has Encrypted key.## JavaScript library method```patientportal.patient.getInsurer();```## HTTP MethodGET## ****Url****/patientportalapi/patient/insurer## Returns[InsurerData](#_InsurerData)