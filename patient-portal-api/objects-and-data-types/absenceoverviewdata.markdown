---
layout: page
title: AbsenceOverviewData
nav_order: 2
parent: Objects and data types
---

# AbsenceOverviewData

A full absence record data object which includes the patient’s full name.

## Properties

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
            <td>Key</td>
            <td>string</td>
            <td>The key of the absence record.</td>
        </tr>
        <tr>
            <td>PatientName</td>
            <td>string</td>
            <td>The name of the patient.</td>
        </tr>
        <tr>
            <td>StartDate</td>
            <td><a href="../objects-and-data-types/datetime">DateTime</a></td>
            <td>The date that the absence started.</td>
        </tr>
        <tr>
            <td>EstimatedEndDate</td>
            <td><a href="../objects-and-data-types/datetime">DateTime</a></td>
            <td>The estimated return-to-work date.</td>
        </tr>
        <tr>
            <td>EndDate</td>
            <td><a href="../objects-and-data-types/datetime">DateTime</a> (optional)</td>
            <td>The actual return-to-work date.</td>
        </tr>
        <tr>
            <td>AbsenceStatusCode</td>
            <td>int</td>
            <td>
                <p>The status code of the absence record.</p>
                <ul>
                    <li>0 – Open</li>
                    <li>2– Closed</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>AbsenceStatusName</td>
            <td>string</td>
            <td>The name of the status code of the absence record, as specified in the AbsenceStatusCode.</td>
        </tr>
        <tr>
            <td>QuestionnaireStatusCode</td>
            <td>int</td>
            <td>
                <p>The status code of the absence.</p>
                <ul>
                    <li>0 – Not Sent</li>
                    <li>1 – Sent</li>
                    <li>2– Completed</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>QuestionnaireStatusName</td>
            <td>string</td>
            <td>
                <p>The name of the status code of the absence record’s questionnaire request, as specified in the
                    QuestionnaireStatusCode.</p>
            </td>
        </tr>
        <tr>
            <td>LostWork</td>
            <td><a href="../objects-and-data-types/lostwork">LostWork</a></td>
            <td>The details about the amount of work lost due to the absence.</td>
        </tr>
        <tr>
            <td>Reason</td>
            <td>string</td>
            <td>The name of the reason for the absence.</td>
        </tr>
        <tr>
            <td>AccidentAtWork</td>
            <td>bool</td>
            <td>Whether the absence was a result of an accident in the workplace.</td>
        </tr>
        <tr>
            <td>ReasonSharedWithEmployer</td>
            <td>bool</td>
            <td>Whether the reason for the absence is to be shared with the employer.</td>
        </tr>
        <tr>
            <td>DepartmentName</td>
            <td>string</td>
            <td>The name of the employee department that the patient belongs to.</td>
        </tr>
        <tr>
            <td>DivisionName</td>
            <td>string</td>
            <td>The name of the employee division that the patient belongs to.</td>
        </tr>
    </tbody>
</table>

## JSON Example

```json
{
    "Key": "efdc81efac0fd1a7f7b1833697a3ec3b",
    "PatientName": "Vercruse, Katarina",
    "DepartmentName": "Support",
    "DivisionName": "Information Technology",
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
```
