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

<table><tbody><tr><th><p>patient</p></th><th><p>string (optional)</p></th><th><p>The key of the patient provided by the API upon GetPatients.</p></th></tr><tr><td><p>due-from</p></td><td><p>DateTime (optional)</p></td><td><p>Due date filter..</p></td></tr><tr><td><p>due-to</p></td><td><p>DateTime (optional)</p></td><td><p>Due date filter.</p></td></tr><tr><td><p>page-sort-column</p></td><td><p>int (optional)</p></td><td><p>The column index to sort the result:</p><ul><li>0 – Due date</li><li>1 – Created date</li><li>2 – Reminder date</li><li>3 – Appointment type name</li></ul><p>Default: 0</p></td></tr><tr><td><p>page-sort-descending</p></td><td><p>int (optional)</p></td><td><p>True to sort result descending.</p></td></tr><tr><td><p>page-number</p></td><td><p>int (optional)</p></td><td><p>Required page number. Default 1.</p></td></tr><tr><td><p>page-size</p></td><td><p>int (optional)</p></td><td><p>Required page size. Default 10. Minimum 5. Maximum 50.</p></td></tr></tbody></table>

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
