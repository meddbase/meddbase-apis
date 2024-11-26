---
layout: page
title: SubmitValidationCode
nav_order: 2
parent: Absence questionnaire
---

# SubmitValidationCode

Validates the patient using the code sent to them via a SMS message received because of a request sent to the [SendValidationSMS](#_SendValidationSMS) method.

## JavaScript library method

```
patientportal.rtwQuestionnaire.submitValidationCode ({

key: &lt;key&gt;.

code: &lt;code&gt;

});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/rtw-questionnaire/submit-validation-code

## URL Parameters

| key | string | The absence key. |
| --- | --- | --- |
| code | string | The code sent to the patient via a SMS message received because of a request sent to the [SendValidationSMS](#_SendValidationSMS) method. |

## Returned JSON

```
{

"status": "ok",

"result": {

<[AbsenceRTWQuestionnaireData](#_AbsenceRTWQuestionnaireData)\>

}

}
```
