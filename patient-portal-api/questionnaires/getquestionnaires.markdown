---
layout: page
title: GetQuestionnaires
nav_order: 3
parent: Questionnaires
---

# GetQuestionnaires

Returns the list of requested questionnaires. Questionnaires requested together (with or without a specific module) are listed together.

## JavaScript library method

```javascript
patientportal.questionnaires.getQuestionnaires({
    patient: <patient>,
    category: ‘ppq’,
    status: <status>,
    pageSortColumn: <page-sort-column>,
    pageSortDescending: <page-sort-descending>,
    pageNumber: <page-number>,
    pageSize: <page-size>
});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/questionnaires/questionnaires

## URL Parameters

<table><tbody><tr><th><p>patient</p></th><th><p>string (optional)</p></th><th><p>The key of the patient provided by the API upon GetPatients.</p></th></tr><tr><td><p>category</p></td><td><p>string (required)</p></td><td><p>Always ‘ppq’</p></td></tr><tr><td><p>status</p></td><td><p>int (optional)</p></td><td><p>Status code filter.</p></td></tr><tr><td><p>page-sort-column</p></td><td><p>int (optional)</p></td><td><p>The column index to sort the result:</p><ul><li>0 – Created order</li><li>1 – Status</li></ul><p>Default: 0</p></td></tr><tr><td><p>page-sort-descending</p></td><td><p>int (optional)</p></td><td><p>True to sort result descending.</p></td></tr><tr><td><p>page-number</p></td><td><p>int (optional)</p></td><td><p>Page number. Default 1.</p></td></tr><tr><td><p>page-size</p></td><td><p>int (optional)</p></td><td><p>Page size. Default 10. Minimum 5. Maximum 50.</p></td></tr></tbody></table>

## Returned JSON

```
{

"Items": \[

<list of [QuestionnaireOverviewData](#_QuestionnaireOverviewData)\>

\]

"TotalCount":24,

"CurrentPage":1,

"PageSize":10,

"SortColumn": 0,

"SortDescending": false

}
```
