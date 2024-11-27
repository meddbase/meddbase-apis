---
layout: page
title: ReferralOverviewData
nav_order: 76
parent: Objects and data types
---

# ReferralOverviewData

Provides overview information about the referral.

## Properties

<table><tbody><tr><th><p>Key</p></th><th><p>string</p></th><th><p>The key of the referral.</p></th></tr><tr><td><p>PatientName</p></td><td><p>string</p></td><td><p>The name of the patient.</p></td></tr><tr><td><p>PatientKey</p></td><td><p>string</p></td><td><p>The key of the patient.</p></td></tr><tr><td><p>ReferredBy</p></td><td><p>string</p></td><td><p>The name of the referrer.</p></td></tr><tr><td><p>CreatedDate</p></td><td><p>string</p></td><td><p>Created date.</p></td></tr><tr><td><p>ModifiedDate</p></td><td><p>string</p></td><td><p>Last modification date.</p></td></tr><tr><td><p>State</p></td><td><p>string</p></td><td><p>The state of the referral:</p><ul><li>QuestionnaireRequired – the referral questionnaire hasn’t been finished.</li><li>AttachDocuments – the referral hasn’t been sent. The user may attach documents and send the referral.</li><li>InProgress – the referral in progress. No user action is needed.</li><li>Completed – the referral is completed.</li></ul><p>The list of states is not complete. There may be also another states.</p></td></tr><tr><td><p>StateDisplayName</p></td><td><p>string</p></td><td><p>The friendly name of the state.</p></td></tr><tr><td><p>StateColor</p></td><td><p>string</p></td><td><p>The color of the state.</p></td></tr><tr><td><p>IsFollowUp</p></td><td><p>bool</p></td><td><p>The referral is a follow up for the previous referral.</p></td></tr><tr><td><p>HasFollowUp</p></td><td><p>bool</p></td><td><p>The referral has a follow up referral.</p></td></tr><tr><td><p>PreviousReferralKey</p></td><td><p>bool</p></td><td><p>The key of the previous referral if IsFollowUp is true.</p></td></tr><tr><td><p>NextReferralKey</p></td><td><p>bool</p></td><td><p>The key of the next referral if HasFollowUp is true.</p></td></tr><tr><td><p>SLARequired</p></td><td><p>bool</p></td><td><p>True if the SLA has been required for the referral.</p></td></tr><tr><td><p>SLAFailed</p></td><td><p>bool</p></td><td><p>True if the SLA has failed for this referral.</p></td></tr><tr><td><p>SLAFailedReason</p></td><td><p>string</p></td><td><p>The reason why SLA failed.</p></td></tr><tr><td><p>ReferralNumber</p></td><td><p>string</p></td><td><p>The number of the referral.</p></td></tr><tr><td><p>AppointmentType</p></td><td><p>AppointmentTypeData</p></td><td><p>The type of the referral.</p></td></tr><tr><td><p>AbsenceRecordKey</p></td><td><p>string</p></td><td><p>The key of the absence record the referral is joined to.</p></td></tr><tr><td><p>DaysToReviewDischargeLetterByPatient</p></td><td><p>int</p></td><td><p>The number of days a patient has to review the referral discharge letter.</p></td></tr></tbody></table>

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
