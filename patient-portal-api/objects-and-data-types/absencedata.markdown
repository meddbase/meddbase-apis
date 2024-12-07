---
layout: page
title: AbsenceData
nav_order: 1
parent: Objects and data types
---

# AbsenceData

A full absence record data object which includes full patient demographic data.

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
            <td>Patient</td>
            <td><a href="../objects-and-data-types/persondemographicdata">PatientDemographicData</a></td>
            <td>The patient’s demographic details.</td>
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
                    <li>1 – Deleted</li>
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
    </tbody>
</table>

## JSON Example

```json
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
```
