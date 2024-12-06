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

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/cases/cases` |

## URL Parameters

<table>
    <thead>
        <tr>
            <th style="text-align: left">Parameter</th>
            <th style="text-align: left">Type</th>
            <th style="text-align: left">Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>patient</td>
            <td>string (optional)</td>
            <td>The patient’s key id.</td>
        </tr>
        <tr>
            <td>text</td>
            <td>string (optional)</td>
            <td>Checks if any of the attributes of the CaseOverviewData object contain <text>.</td>
        </tr>
        <tr>
            <td>status</td>
            <td>int (optional)</td>
            <td>
                <ol>
                    <li>No filter (Default)</li>
                    <li>Open cases</li>
                    <li>Closed cases</li>
                </ol>
            </td>
        </tr>
        <tr>
            <td>case</td>
            <td>int (optional)</td>
            <td>The case’s key id.</td>
        </tr>
        <tr>
            <td>title</td>
            <td>string (optional)</td>
            <td>The public title of the case.</td>
        </tr>
        <tr>
            <td>patientName</td>
            <td>string (optional)</td>
            <td>The patient’s name.</td>
        </tr>
        <tr>
            <td>department</td>
            <td>string (optional)</td>
            <td>Key of the department provided by the API upon GetDepartments.</td>
        </tr>
        <tr>
            <td>division</td>
            <td>string (optional)</td>
            <td>Key of the division provided by the API upon GetDepartments.</td>
        </tr>
        <tr>
            <td>page-sort-column</td>
            <td>int (optional)</td>
            <td>
                <p>The column index to sort the result:</p>
                <ol>
                    <li>Case Key</li>
                    <li>Person Name</li>
                    <li>Case Title</li>
                    <li>Opened Date</li>
                    <li>Closed Date</li>
                    <li>Last Updated Date</li>
                </ol>
                <p>By default the result is sorted by last updated date.</p>
            </td>
        </tr>
        <tr>
            <td>page-sort-descending</td>
            <td>int (optional)</td>
            <td>True to sort result descending.</td>
        </tr>
        <tr>
            <td>page-number</td>
            <td>int (optional)</td>
            <td>Page number. Default 1.</td>
        </tr>
        <tr>
            <td>page-size</td>
            <td>int (optional)</td>
            <td>Page size. Default 5. Minimum 5. Maximum 50.</td>
        </tr>
    </tbody>
</table>

## Returns

[CaseOverviewData](../objects-and-data-types/caseoverviewdata)[]

## Returned JSON

```json
{
    "Items": [
        {
            "Key": 11229,
            "PatientName": "Lemon, John",
            "OpenedDate": "2024-01-01T09:30:00",
            "Title": "1st Case for this Patient",
            "LastUpdatedDate": "2024-01-01T09:30:00",
            "IsOpen": true
        }
    ],
    "TotalCount": 15,
    "CurrentPage": 1,
    "PageSize": 10,
    "SortColumn": 0,
    "SortDescending": false
}
```
