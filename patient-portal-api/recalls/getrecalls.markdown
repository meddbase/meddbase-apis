---
layout: page
title: GetRecalls
nav_order: 1
parent: Recalls
---

# GetRecalls

Returns the list of recalls.

## JavaScript library method

```javascript
patientportal.recalls.getRecalls({
    patient: <patient>,
    dueFrom: <due-from>,
    dueTo: <due-to>,
    pageSortColumn: <page-sort-column>,
    pageSortDescending: <page-sort-descending>,
    pageNumber: <page-number>,
    pageSize: <page-size>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/recalls/recalls` |

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
            <td>due-from</td>
            <td><a href="../objects-and-data-types/datetime">DateTime</a> (optional)</td>
            <td>Due date filter..</td>
        </tr>
        <tr>
            <td>due-to</td>
            <td><a href="../objects-and-data-types/datetime">DateTime</a> (optional)</td>
            <td>Due date filter.</td>
        </tr>
        <tr>
            <td>page-sort-column</td>
            <td>int (optional)</td>
            <td>
                <p>The column index to sort the result:</p>
                <ul>
                    <li>0 – Due date</li>
                    <li>1 – Created date</li>
                    <li>2 – Reminder date</li>
                    <li>3 – Appointment type name</li>
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
            <td>Required page number. Default 1.</td>
        </tr>
        <tr>
            <td>page-size</td>
            <td>int (optional)</td>
            <td>Required page size. Default 10. Minimum 5. Maximum 50.</td>
        </tr>
    </tbody>
</table>

## Returns

[RecallData](../objects-and-data-types/recalldata)[]

## Returned JSON

```json
{
    "Items": [
        {
            "Key": "3bdd966cf6f9c0c6872ee0551da74c4d",
            "DueDate": "2017-03-14T00:00:00",
            "Reason": "Test",
            "AppointmentType": {
                "Key": "CN",
                "Name": "Consultation",
                "CancellationPolicy": "You will be charged at 50% of the full price if you cancel the appointment within 72 hours. You will be charged at 90% of the full price if you do not turn up.",
                "CanBookAppointment": true,
                "CanReferPatient": false,
                "TelemedicineOption": true,
                "CanAddServices": false
            },
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
            "Clinician": {
                "Key": 84,
                "FullName": "Dr. House"
            }
        }
    ],
    "TotalCount":24,
    "CurrentPage":1,
    "PageSize":10,
    "SortColumn": 0,
    "SortDescending": false
}
```
