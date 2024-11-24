---
layout: page
title: \[DEPRECATED\] SubmitValidationSMS
nav_order: 18
parent: Authentication
---

# \[DEPRECATED\] SubmitValidationSMSThis method has been deprecated. Please use SubmitActicationSMS.Submits the validation number from the validation SMS and returns confirmation.## JavaScript library method```patientportal.auth.submitValidationSMS({code: &lt;code&gt;, mobile: &lt;mobile&gt;, isOH: &lt;is-oh&gt;});```## HTTP MethodGET## ****Url****/patientportalapi/auth/submit-validation-sms## URL Parameters| code | string | Validation code. || --- | --- | --- || mobile | string | Patient’s mobile telephone number. || is-oh | bool | True for the referral portal. False for the patient portal. |## ReturnsActivationConfirmation## RemarksIf the activation is completed successfully the API returns the confirmation object. The confirmation may include the outstanding invoice (usually the membership fee) that should be paid. To pay for the invoice the client needs to call ProvidePayment method.