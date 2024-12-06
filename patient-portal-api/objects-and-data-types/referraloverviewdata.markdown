---
layout: page
title: ReferralOverviewData
nav_order: 76
parent: Objects and data types
---

# ReferralOverviewData

Provides overview information about the referral.

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
            <td>The key of the referral.</td>
        </tr>
        <tr>
            <td>PatientName</td>
            <td>string</td>
            <td>The name of the patient.</td>
        </tr>
        <tr>
            <td>PatientKey</td>
            <td>string</td>
            <td>The key of the patient.</td>
        </tr>
        <tr>
            <td>ReferredBy</td>
            <td>string</td>
            <td>The name of the referrer.</td>
        </tr>
        <tr>
            <td>CreatedDate</td>
            <td>string</td>
            <td>Created date.</td>
        </tr>
        <tr>
            <td>ModifiedDate</td>
            <td>string</td>
            <td>Last modification date.</td>
        </tr>
        <tr>
            <td>State</td>
            <td>string</td>
            <td>
                <p>The state of the referral:</p>
                <ul>
                    <li>QuestionnaireRequired – the referral questionnaire hasn’t been finished.</li>
                    <li>AttachDocuments – the referral hasn’t been sent. The user may attach documents and send the
                        referral.</li>
                    <li>InProgress – the referral in progress. No user action is needed.</li>
                    <li>Completed – the referral is completed.</li>
                </ul>
                <p>The list of states is not complete. There may be also another states.</p>
            </td>
        </tr>
        <tr>
            <td>StateDisplayName</td>
            <td>string</td>
            <td>The friendly name of the state.</td>
        </tr>
        <tr>
            <td>StateColor</td>
            <td>string</td>
            <td>The color of the state.</td>
        </tr>
        <tr>
            <td>IsFollowUp</td>
            <td>bool</td>
            <td>The referral is a follow up for the previous referral.</td>
        </tr>
        <tr>
            <td>HasFollowUp</td>
            <td>bool</td>
            <td>The referral has a follow up referral.</td>
        </tr>
        <tr>
            <td>PreviousReferralKey</td>
            <td>bool</td>
            <td>The key of the previous referral if IsFollowUp is true.</td>
        </tr>
        <tr>
            <td>NextReferralKey</td>
            <td>bool</td>
            <td>The key of the next referral if HasFollowUp is true.</td>
        </tr>
        <tr>
            <td>SLARequired</td>
            <td>bool</td>
            <td>True if the SLA has been required for the referral.</td>
        </tr>
        <tr>
            <td>SLAFailed</td>
            <td>bool</td>
            <td>True if the SLA has failed for this referral.</td>
        </tr>
        <tr>
            <td>SLAFailedReason</td>
            <td>string</td>
            <td>The reason why SLA failed.</td>
        </tr>
        <tr>
            <td>ReferralNumber</td>
            <td>string</td>
            <td>The number of the referral.</td>
        </tr>
        <tr>
            <td>AppointmentType</td>
            <td><a href="../objects-and-data-types/appointmenttypedata">AppointmentTypeData</a></td>
            <td>The type of the referral.</td>
        </tr>
        <tr>
            <td>AbsenceRecordKey</td>
            <td>string</td>
            <td>The key of the absence record the referral is joined to.</td>
        </tr>
        <tr>
            <td>DaysToReviewDischargeLetterByPatient</td>
            <td>int</td>
            <td>The number of days a patient has to review the referral discharge letter.</td>
        </tr>
    </tbody>
</table>

## JSON Example

```json
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
```
