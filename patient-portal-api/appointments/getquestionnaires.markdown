---
layout: page
title: GetQuestionnaires
nav_order: 14
parent: Appointments
---

# GetQuestionnaires

Gets all questionnaires for future appointments based on filters. Gets complete, incomplete and partially complete questionnaires.

## JavaScript library method

```javascript
patientportal.appointment.getQuestionnaires({
    patient: <patient>,
    questionnaireTypeName: <questionnaire-type-name>,
    expirationFrom: <expiration-from>,
    expirationTo: < expiration-to>,
    status: <status>,
    appointment: <appointmentId>,
    pageSortColumn: <page-sort-column>,
    pageSortDescending: <page-sort-descending>,
    pageNumber: <page-number>,
    pageSize: <page-size>
});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/appointment/questionnaires

## URL Parameters

<table><tbody><tr><th><p>patient</p></th><th><p>string (optional)</p></th><th><p>The key of the patient provided by the API upon section Patients.</p><p>Default is undefined which returns questionnaires for all patients.</p></th></tr><tr><td><p>questionnaire-type-name</p></td><td><p>string (optional)</p></td><td><p>The questionnaire type name filter. Optional if appointment id is provided</p></td></tr><tr><td><p>expiration-from</p></td><td><p>DateTime (optional)</p></td><td><p>The questionnaire start date filter.</p></td></tr><tr><td><p>expiration-to</p></td><td><p>DateTime (optional)</p></td><td><p>The questionnaire start date filter.</p></td></tr><tr><td><p>status</p></td><td><p>int (optional)</p></td><td><p>Status code of the questionnaire:</p><ul><li>0 = Incomplete</li><li>1 = Complete</li><li>2 = Partially Complete</li><li>-1 = all</li></ul><p>Default: -1</p></td></tr><tr><td><p>appointment</p></td><td><p>Int<br>(optional)</p></td><td><p>Appointment id to get questionnaires of a booked appointment. Optional if questionnaire name is provided.</p></td></tr><tr><td><p>page-sort-column</p></td><td><p>int (optional)</p></td><td><p>The column index to sort the result:</p><ul><li>0 –Expiration date</li><li>1 – Status</li></ul><p>Default: 0</p></td></tr><tr><td><p>page-sort-descending</p></td><td><p>int (optional)</p></td><td><p>True to sort result descending. Default false.</p></td></tr><tr><td><p>page-number</p></td><td><p>int (optional)</p></td><td><p>Required page number. Default 1.</p></td></tr><tr><td><p>page-size</p></td><td><p>int (optional)</p></td><td><p>Required page size. Default 10. Minimum 5. Maximum 50.</p></td></tr></tbody></table>

## Returned JSON

```
{

"Items": \[

<list of QuestionnaireOverviewData>

\]

"TotalCount":24,

"CurrentPage":1,

"PageSize":10,

"SortColumn": 0,

"SortDescending": false

}
```

## Remarks

Overview data doesn’t contain definitions of questionnaires (questionnaire markup). The client has to call GetQuestionnaireDetail to retrieve it.
