---
layout: page
title: GetDepartmentsAndDivisions
nav_order: 25
parent: Authentication
---

# GetDepartmentsAndDivisionsReturns the list of employer departments and divisions.## JavaScript library method```patientportal.auth.getDepartmentsAndDivisions({regCode: &lt;reg-code&gt;, isOH: &lt;is-oh&gt;});```## HTTP MethodGET## ****Url****/patientportalapi/auth/departments-divisions## URL Parameters| reg-code | string | Online referral portal sign up access code that is provided to the manager. || --- | --- | --- || is-oh | bool | True for the referral portal. False for the patient portal. |## Returned JSON```{"Departments": \[&lt;list of DepartmentData&gt;\]"Divisions": \[&lt;list of DivisionData&gt;\]}```## RemarksFor patient portal, providing departments and divisions during registration setting needs to enabled. If the code isn’t the sign up code or the settings is disabled, an exception is thrown.