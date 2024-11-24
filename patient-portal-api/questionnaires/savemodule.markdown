---
layout: page
title: SaveModule
nav_order: 5
parent: Questionnaires
---

# SaveModuleCreate or update a module. Modules can only be shared if the logged in user has the _CanModifyQuestionnaireForms_ right. Returns the key of the module created.## JavaScript library method```patientportal.questionnaires. saveModule ({moduleKey: &lt;module-key&gt;,category: &lt;’ppq’&gt;,moduleName: &lt;module-name&gt;,shared: &lt;shared&gt;,formKeys: &lt;form-keys&gt;});```## HTTP MethodPOST## ****Url****/patientportalapi/questionnaires/save-module## URL Parameters| module-key | string (optional) | The key of the module provided by the API upon [GetModules](#_GetModules) or a previous call to SaveModule. If not specified, a new module will be created. || --- | --- | --- || category | string (required) | Always ‘ppq’. || module-name | string (required) | Module name. || shared | bool (optional) | Share the module with other users. Default false. |## POST Parameters| form-keys | string\[\] (required) | List of form keys returned from [GetQuestionnaireForms](#_GetQuestionnaireForms). || --- | --- | --- |## Returned JSON```“ae71266c1548673052d1240115466e63a8ece5c5d3cf06abe1d006f7d975ff76”```