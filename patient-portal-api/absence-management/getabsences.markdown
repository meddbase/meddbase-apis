---
layout: page
title: GetAbsences
nav_order: 1
parent: Absence Management
---

# GetAbsences
Returns a list of absence records filtered by any of the optional parameters specified. Does not show deleted absences.

## JavaScript library method

```javascript
patientportal.absences.getAbsences({
    patient: <patient>,
    from: <date-from>,
    to: <date-to>,
    status: <status>,
    text: <text>,
    department: <department>,
    division: <division>,
    questionnaireStatus: <questionnaire-status>,
    pageSortColumn: <page-sort-column>,
    pageSortDescending: <page-sort-descending>,
    pageNumber: <page-number>,
    pageSize: <page-size>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/absences/absences` |

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
            <td>The absentee’s key id.</td>
        </tr>
        <tr>
            <td>date-from</td>
            <td><a href="../objects-and-data-types/datetime">DateTime</a> (optional)</td>
            <td>The earliest date to look for absences.</td>
        </tr>
        <tr>
            <td>date-to</td>
            <td><a href="../objects-and-data-types/datetime">DateTime</a> (optional)</td>
            <td>The latest date to look for absences.</td>
        </tr>
        <tr>
            <td>status</td>
            <td>int (optional)</td>
            <td>Open = 0, Closed = 2 (Deleted absences are not shown in the API, so cannot be filtered for).</td>
        </tr>
        <tr>
            <td>text</td>
            <td>string (optional)</td>
            <td>
                <p>Checks if any of the following attributes of the absentee starts with the specified text: Surname,
                    Name, WorkEmail, Email, LegacyNr.</p>
            </td>
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
            <td>questionnaireStatus</td>
            <td>int (optional)</td>
            <td>0 = Not Sent, 1 = Sent, 2 = Completed.</td>
        </tr>
        <tr>
            <td>page-sort-column</td>
            <td>int (optional)</td>
            <td>
                <p>The column index to sort the result:</p>
                <ul>
                    <li>0 – From date</li>
                    <li>1 – To date</li>
                    <li>2– Reason</li>
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
            <td>Page size. Default 5. Minimum 5. Maximum 50.</td>
        </tr>
    </tbody>
</table>

## Returns

[AbsenceData](../objects-and-data-types/absencedata)[]

## Returned JSON

```json
{
    "status": "ok",
    "result": {
        "Items": [
            {
                "Patient": {
                    "Title": "Mr",
                    "Name": "John",
                    "Surname": "Lemon",
                    "SexType": 1,
                    "Initials": "JL",
                    "DateOfBirth": "1958-08-02T00:00:00",
                    "Mobile": "+444 895 523 411",
                    "Telephone": "+444 525 111 555",
                    "EmailAddress": "<john.lemon@test.com>",
                    "WorkEmailAddress": "<john.lemon@mywork.com>",
                    "Address": {
                        "Address1": "Studio 99",
                        "Address2": "Backlok Street",
                        "Address3": "Camden",
                        "City": "London",
                        "County": "",
                        "PostCode": "N1 7NK",
                        "Country": "United Kingdom"
                    }
                },
                "Key": "efdc81efac0fd1a7f7b1833697a3ec3b",
                "StartDate": "2018-06-11T00:00:00",
                "EstimatedEndDate": "2018-06-15T00:00:00",
                "EndDate": "2018-06-15T00:00:00",
                "AbsenceStatusCode": 2,
                "AbsenceStatusName": "Closed",
                "QuestionnaireStatusCode": 0,
                "QuestionnaireStatusName": "Not sent",
                "LostWork": {
                    "Hours": 32,
                    "Days": 4
                },
                "Reason": "Brain Tumour",
                "AccidentAtWork": false,
                "ReasonSharedWithEmployer": true
            }
        ],
        "TotalCount": 15,
        "CurrentPage": 1,
        "PageSize": 10,
        "SortColumn": 0,
        "SortDescending": false
    }
}
```
