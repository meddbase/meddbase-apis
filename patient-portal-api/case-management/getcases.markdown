---
layout: page
title: GetCases
nav_order: 1
parent: Case Management
---

# GetCases

Returns a list of cases filtered by any of the optional parameters specified.

## JavaScript library method

```javascript
patientportal.cases.getCases({
    patient: <patient>,
    text: <text>,
    status: <status>,
    case: <case>,
    title: <title>,
    patientName: <patient-name>,
    department: <department>,
    division: <division>,
    pageSortColumn: <page-sort-column>,
    pageSortDescending: <page-sort-descending>,
    pageNumber: <page-number>,
    pageSize: <page-size>
});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/cases/cases

## URL Parameters

<table><tbody><tr><th><p>patient</p></th><th><p>string (optional)</p></th><th><p>The patient’s key id.</p></th></tr><tr><td><p>text</p></td><td><p>string (optional)</p></td><td><p>Checks if any of the attributes of the CaseOverviewData object contain <text>.</p></td></tr><tr><td><p>status</p></td><td><p>int (optional)</p></td><td><ol><li>No filter (Default)</li><li>Open cases</li><li>Closed cases</li></ol></td></tr><tr><td><p>case</p></td><td><p>Int (optional)</p></td><td><p>The case’s key id.</p></td></tr><tr><td><p>title</p></td><td><p>string (optional)</p></td><td><p>The public title of the case.</p></td></tr><tr><td><p>patientName</p></td><td><p>string (optional)</p></td><td><p>The patient’s name.</p></td></tr><tr><td><p>department</p></td><td><p>string (optional)</p></td><td><p>Key of the department provided by the API upon GetDepartments.</p></td></tr><tr><td><p>division</p></td><td><p>string (optional)</p></td><td><p>Key of the division provided by the API upon GetDepartments.</p></td></tr><tr><td><p>page-sort-column</p></td><td><p>int (optional)</p></td><td><p>The column index to sort the result:</p><ol><li>Case Key</li><li>Person Name</li><li>Case Title</li><li>Opened Date</li><li>Closed Date</li><li>Last Updated Date</li></ol><p>By default the result is sorted by last updated date.</p></td></tr><tr><td><p>page-sort-descending</p></td><td><p>int (optional)</p></td><td><p>True to sort result descending.</p></td></tr><tr><td><p>page-number</p></td><td><p>int (optional)</p></td><td><p>Page number. Default 1.</p></td></tr><tr><td><p>page-size</p></td><td><p>int (optional)</p></td><td><p>Page size. Default 5. Minimum 5. Maximum 50.</p></td></tr></tbody></table>

## Returned JSON

```
{

"Items": \[

<list of CaseOverviewData>

\],

"TotalCount": 15,

"CurrentPage": 1,

"PageSize": 10,

"SortColumn": 0,

"SortDescending": false

}
```
