---
layout: page
title: DeleteModule
nav_order: 6
parent: Questionnaires
---

# DeleteModuleDelete the specified module. The user must have the _CanModifyQuestionnaireForms_ right.## JavaScript library method```patientportal.questionnaires.getQuestionnaires({moduleKey: &lt;module-key&gt;});```## HTTP MethodGET## ****Url****/patientportalapi/questionnaires/delete-module## URL Parameters| module-key | string (required) | The key of the patient provided by the API upon [GetModules](#_GetModules). || --- | --- | --- |