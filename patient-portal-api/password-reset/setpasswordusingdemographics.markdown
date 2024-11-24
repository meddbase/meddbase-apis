---
layout: page
title: \[OBSOLETE\] SetPasswordUsingDemographics
nav_order: 6
parent: Password reset
---

# \[OBSOLETE\] SetPasswordUsingDemographicsSets the new password using the demographics match verification. This method is supported for legacy reasons and will be removed in the future.## JavaScript library method```patientportal.auth.setPasswordUsingDemographics({key: &lt;key&gt;,name: &lt;name&gt;,surname: &lt;surname&gt;,dateOfBirth: &lt;dateOfBirth&gt;,postcode: &lt;postcode&gt;,newPassword: &lt;newPassword&gt;});```## HTTP MethodPOST## ****Url****/patientportalapi/auth/set-password-using-demographics## URL Parameters| Is-oh | bool | True for the referral portal. False for the patient portal. || --- | --- | --- |## POST Parameters| key | string | Reset key that is included in the URL. || --- | --- | --- || name | string | Patient’s name. || surname | string | Patient’s surname. || dateOfBirth | DateTime | Patient’s date of birth. || postcode | string | Patient’s address postcode. || newPassword | string | New password for patient’s account. |