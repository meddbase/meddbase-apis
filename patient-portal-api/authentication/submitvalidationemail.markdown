---
layout: page
title: \[DEPRECATED\] SubmitValidationEmail
nav_order: 16
parent: Authentication
---

# \[DEPRECATED\] SubmitValidationEmailThis method has been deprecated. Please use SubmitActivationEmail.Submits the confirmation key that the client retrieves from the URL and returns confirmation.## JavaScript library method```patientportal.auth.submitValidationEmail({key: &lt;key&gt;, isOH: &lt;is-oh&gt;});```## HTTP MethodGET## ****Url****/patientportalapi/auth/submit-validation-email## URL Parameters| key | string | Confirmation key that is included in the URL. || --- | --- | --- || is-oh | bool | True for the referral portal. False for the patient portal. |## ReturnsActivationConfirmation## RemarksIf the activation is completed successfully the API returns the confirmation object. The confirmation may include the outstanding invoice (usually the membership fee) that should be paid. To pay for the invoice the client needs to call ProvidePayment method.