---
layout: page
title: GetQuestionnaireForms
nav_order: 1
parent: Questionnaires
---

# GetQuestionnaireFormsReturns the list of questionnaire forms that can be requested for any patient. If a module is specified then only the forms included in that module are returned.## JavaScript library method```patientportal.questionnaires. getQuestionnaireForms ({moduleKey: &lt;module-key&gt;,category: &lt;’ppq’&gt;,formName: &lt;form-name&gt;,pageNumber: &lt;page-number&gt;,pageSize: &lt;page-size&gt;});```## HTTP MethodGET## ****Url****/patientportalapi/questionnaires/forms## URL Parameters| module-key | string (optional) | The key of the module provided by the API upon GetModules. || --- | --- | --- || category | string (required) | Always ‘ppq’. || form-name | string (optional) | Filter for form name. || page-number | int (optional) | Page number. Default 1. || page-size | int (optional) | Page size. Default 10. Minimum 5. Maximum 50. |## Returned JSON```{"Items": \[<list of [QuestionnaireFormData](#_QuestionnaireFormData)\>\]"TotalCount":24,"CurrentPage":1,"PageSize":10}```