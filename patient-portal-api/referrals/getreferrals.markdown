---
layout: page
title: GetReferrals
nav_order: 1
parent: Referrals
---

# GetReferrals

Returns the referrals that meets the search criteria.

## JavaScript library method

```javascript
patientportal.referrals.getReferrals({
    patient: <patient>,
    text: <text>,
    status: <status>,
    referralNumber: <referral-number>,
    patientName: <patient-name>,
    referrerName: <referrer-name>,
    department: <department>,
    division: <division>,
    case: <case>,
    pageSortColumn: <page-sort-column>,
    pageSortDescending: <page-sort-descending>,
    pageNumber: <page-number>,
    pageSize: <page-size>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/referrals/referrals` |

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
            <td>text</td>
            <td>string (optional)</td>
            <td>
                <p>Any text the API will try to filter by patient’s/referrer’s name, email, employee number or by
                    referral number if the text is a number.</p>
            </td>
        </tr>
        <tr>
            <td>status</td>
            <td>int (optional)</td>
            <td>
                <p>Status filter:</p>
                <ul>
                    <li>0 – &lt;disabled, filter no active&gt;</li>
                    <li>1 – Questionnaire required</li>
                    <li>2 – Documents required</li>
                    <li>3 – In progress</li>
                    <li>4 – Closed only</li>
                    <li>5 – Opened only</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>referral-number</td>
            <td>string (optional)</td>
            <td>The number of the referral.</td>
        </tr>
        <tr>
            <td>patient-name</td>
            <td>string (optional)</td>
            <td>The patient name.</td>
        </tr>
        <tr>
            <td>referrer-name</td>
            <td>string (optional)</td>
            <td>The referrer name.</td>
        </tr>
        <tr>
            <td>department</td>
            <td>string (optional)</td>
            <td>Key of the department provided by the API upon <a href="../patient/getdepartmentsanddivisions">GetDepartmentsAndDivisions</a>.</td>
        </tr>
        <tr>
            <td>division</td>
            <td>string (optional)</td>
            <td>Key of the division provided by the API upon <a href="../patient/getdepartmentsanddivisions">GetDepartmentsAndDivisions</a>.</td>
        </tr>
        <tr>
            <td>case</td>
            <td>int (optional)</td>
            <td>The case key for the referral.</td>
        </tr>
        <tr>
            <td>page-sort-column</td>
            <td>int (optional)</td>
            <td>
                <p>The column index to sort the result:</p>
                <ul>
                    <li>0 – Last modification date</li>
                    <li>1 – Referral number</li>
                    <li>2 – Patient name</li>
                    <li>3 – Referrer name</li>
                    <li>4 – Date created</li>
                </ul>
                <p>By default the result is sorted by last modification date.</p>
            </td>
        </tr>
        <tr>
            <td>page-sort-descending</td>
            <td>int (optional)</td>
            <td>True to sort result descending. Note that this parameter is ignored for column index 0.</td>
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

[ReferralOverviewData](../objects-and-data-types/referraloverviewdata)[]

## Returned JSON

```json
{
    "Items": [
        {
            "Key": "R123",
            "PatientName": "Mr. John Smith",
            "ReferredBy": "Mr. Will Smith",
            "CreatedDate": "2015-03-13T14:22:12",
            "ModifiedDate": "2015-03-13T14:52:30",
            "State": "InProgress",
            "StateDisplayName": "In progress",
            "StateColor": "green",
            "SLARequired": true,
            "SLAFailed": true,
            "SLAFailedReason": "The appointment was not placed within the SLA (5 days): Patient cannot meet SLA.",
            "ReferralNumber": 13911,
            "AppointmentType": {
                "Name": "Referral",
                "Key": "REF1",
                "Notes": "",
                "CanBookAppointment": true,
                "CanReferPatient": true
            },
            "DaysToReviewDischargeLetterByPatient": 3
        }
    ],
    "TotalCount":1,
    "CurrentPage":1,
    "PageSize":10,
    "SortColumn": 0,
    "SortDescending": false
}
```
