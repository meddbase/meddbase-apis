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

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/appointment/questionnaires` |

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
            <td>
                <p>The key of the patient provided by the API upon section <a href="../patients/patients">Patients</a>.</p>
                <p>Default is undefined which returns questionnaires for all patients.</p>
            </td>
        </tr>
        <tr>
            <td>questionnaire-type-name</td>
            <td>string (optional)</td>
            <td>The questionnaire type name filter. Optional if appointment id is provided</td>
        </tr>
        <tr>
            <td>expiration-from</td>
            <td><a href="../objects-and-data-types/datetime">DateTime</a> (optional)</td>
            <td>The questionnaire start date filter.</td>
        </tr>
        <tr>
            <td>expiration-to</td>
            <td><a href="../objects-and-data-types/datetime">DateTime</a> (optional)</td>
            <td>The questionnaire start date filter.</td>
        </tr>
        <tr>
            <td>status</td>
            <td>int (optional)</td>
            <td>
                <p>Status code of the questionnaire:</p>
                <ul>
                    <li>0 = Incomplete</li>
                    <li>1 = Complete</li>
                    <li>2 = Partially Complete</li>
                    <li>-1 = all</li>
                </ul>
                <p>Default: -1</p>
            </td>
        </tr>
        <tr>
            <td>appointment</td>
            <td>int (optional)</td>
            <td>
                <p>Appointment id to get questionnaires of a booked appointment. Optional if questionnaire name is
                    provided.</p>
            </td>
        </tr>
        <tr>
            <td>page-sort-column</td>
            <td>int (optional)</td>
            <td>
                <p>The column index to sort the result:</p>
                <ul>
                    <li>0 –Expiration date</li>
                    <li>1 – Status</li>
                </ul>
                <p>Default: 0</p>
            </td>
        </tr>
        <tr>
            <td>page-sort-descending</td>
            <td>int (optional)</td>
            <td>True to sort result descending. Default false.</td>
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
    "TotalCount":1,
    "CurrentPage":1,
    "PageSize":10,
    "SortColumn": 0,
    "SortDescending": false
}
```

## Remarks

Overview data doesn’t contain definitions of questionnaires (questionnaire markup). The client has to call [GetQuestionnaireDetail](../appointments/getquestionnairedetail) to retrieve it.
