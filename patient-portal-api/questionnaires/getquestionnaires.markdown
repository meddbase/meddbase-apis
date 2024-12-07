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

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/questionnaires/questionnaires` |

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
            <td>The key of the patient provided by the API upon <a href="../patients/getpatients">GetPatients</a>.</td>
        </tr>
        <tr>
            <td>category</td>
            <td>string (required)</td>
            <td>Always ‘ppq’</td>
        </tr>
        <tr>
            <td>status</td>
            <td>int (optional)</td>
            <td>Status code filter.</td>
        </tr>
        <tr>
            <td>page-sort-column</td>
            <td>int (optional)</td>
            <td>
                <p>The column index to sort the result:</p>
                <ul>
                    <li>0 – Created order</li>
                    <li>1 – Status</li>
                </ul>
                <p>Default: 0</p>
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
            <td>Page size. Default 10. Minimum 5. Maximum 50.</td>
        </tr>
    </tbody>
</table>

## Returns

[QuestionnaireOverviewData](../objects-and-data-types/questionnaireoverviewdata)[]

## Returned JSON

```json
{
    "Items": [
        {
            "Key": "q13788",
            "Name": "Basic questionnaire",
            "Description": "",
            "StatusCode": 0,
            "Status": "Incomplete",
            "AppointmentKey": "apt5821",
            "Expiration": "2013-08-25",
            "Sent": "2013-07-01",
            "ReferralKey": "8ebb55f10382d73e494e7207d1bd7272",
            "CanRefer": 0
        }
    ],
    "TotalCount":24,
    "CurrentPage":1,
    "PageSize":10,
    "SortColumn": 0,
    "SortDescending": false
}
```
