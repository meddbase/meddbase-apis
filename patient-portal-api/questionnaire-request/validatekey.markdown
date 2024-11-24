---
layout: page
title: ValidateKey
nav_order: 4
parent: Questionnaire Request
---

# ValidateKeyValidates whether the security context for the last submitted validation code is still valid.## JavaScript library method```patientportal.questionnaireRequest.validateKey({key: &lt;key&gt;});```## HTTP MethodGET## ****Url****/patientportalapi/questionnaire-request/validate-key## URL Parameters| key | string | The validation key provided in the URL. || --- | --- | --- |## RemarksMethod does not return any data. If something goes wrong please check exception (see Error handling).If the security context runs out the patient may request another validation code and submit it to create new security context.