---
layout: page
title: GetMedialReportData
nav_order: 5
parent: Manager Medical Report Review
---

# GetMedialReportDataReturns the medical report data.The method is only valid if the current temporary security context is valid (see SubmitValidationCode).## JavaScript library method```patientportal.managerReportReview.getMedicalReportData({key: &lt;key&gt;});```## HTTP MethodGET## ****Url****/patientportalapi/manager-report-review/review-data## URL Parameters| key | string | The validation key provided in the URL. || --- | --- | --- |## ReturnsManagerReportReviewData## RemarksIf something goes wrong please check exception (see Error handling).