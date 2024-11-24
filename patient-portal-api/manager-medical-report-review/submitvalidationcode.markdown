---
layout: page
title: SubmitValidationCode
nav_order: 3
parent: Manager Medical Report Review
---

# SubmitValidationCodeSubmits the validation code and returns the medical report review data. Once the validation code is submitted a temporary security context is created.## JavaScript library method```patientportal.managerReportReview.submitValidationCode({key: &lt;key&gt;,code: &lt;code&gt;});```## HTTP MethodGET## ****Url****/patientportalapi/manager-report-review/submit-validation-code## URL Parameters| key | string | The validation key provided in the URL. || --- | --- | --- || code | string | The validation code the manager gets through the email or text message. |## ReturnsManagerReportReviewData## RemarksSubmitting the validation code creates a temporary security context which is valid for 30 minutes. Within this time frame the manager needs to review the medical report and submit the authorisation.The client may use ValidateKey to verify whether the security context runs out and request new validation code to create a new security context.If something goes wrong please check exception (see Error handling).