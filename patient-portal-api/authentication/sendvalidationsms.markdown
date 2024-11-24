---
layout: page
title: \[DEPRECATED\] SendValidationSMS
nav_order: 17
parent: Authentication
---

# \[DEPRECATED\] SendValidationSMSThis method has been deprecated. Please use SendActivationSMS.Sends the validation SMS to the patient’s mobile telephone number.## JavaScript library method```patientportal.auth.sendValidationSMS({mobile: &lt;mobile&gt;, isOH: &lt;is-oh&gt;});```## HTTP MethodGET## ****Url****/patientportalapi/auth/send-validation-sms## URL Parameters| mobile | string | Patient’s mobile telephone number. || --- | --- | --- || is-oh | bool | True for the referral portal. False for the patient portal. |## RemarksSometimes the patient needs to send the validation SMS again because (for example) she deletes it before activating her account.