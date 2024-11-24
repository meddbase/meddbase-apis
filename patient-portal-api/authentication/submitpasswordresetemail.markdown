---
layout: page
title: \[DEPRECATED\] SubmitPasswordResetEmail
nav_order: 20
parent: Authentication
---

# \[DEPRECATED\] SubmitPasswordResetEmailThis method has been deprecated. Please see Password reset section for more details.Submit the password reset key that the client retrieves from the URL and additional information that the client collets from the patient.## JavaScript library method```patientportal.auth.submitPasswordResetEmail({key: &lt;key&gt;,name: &lt;name&gt;,surname: &lt;surname&gt;,dateOfBirth: &lt;date-of-birth&gt;,postcode: &lt;postcode&gt;,newPassword: &lt;new-password&gt;,isOH: &lt;is-oh&gt;});```## HTTP MethodPOST## ****Url****/patientportalapi/auth/submit-password-reset-email## URL Parameters| is-oh | bool | True for the referral portal. False for the patient portal. || --- | --- | --- |## POST Parameters| key | string | Reset key that is included in the URL. || --- | --- | --- || name | string | Patient’s name. || surname | string | Patient’s surname. || dateOfBirth | DateTime | Patient’s date of birth. || postcode | string | Patient’s address postcode. || newPassword | string | New password for patient’s account. |