---
layout: page
title: ReferralData
nav_order: 75
parent: Objects and data types
---

# ReferralData

Provides full information about the referral. Includes all properties of the ReferralOverviewData.

## Properties

| &lt;ReferralOverviewData properties&gt; |     | The object inherits the ReferralOverviewData |
| --- | --- | --- |
| Appointments | AppointmentData\[\] | List of appointments related to the referral. |
| Questionnaires | QuestionnaireOverviewData\[\] | List of questionnaires related to the referral. |
| Documents | DocumentData\[\] | List of attached documents. |
| CanBookAppointment | bool | Defines whether the user has got right to book an appointment directly. |
| CanCancel | bool | Defines whether the user has got right to cancel the referral. |
| CanSend | bool | Defines whether the user has got right to send the referral. |
| CanReallocate | bool | Defines whether the user has got right to reallocate the referral. |
| CanCollaborate | bool | Defines whether the user has got right to collaborate. |
| CanAttachDocuments | bool | Defines whether the user has got right to attach documents. |
| CanFollowUp | bool | Defines whether the user has got right to request the follow up. |
| PatientReview | PatientReportReviewState (optional) | The state of the patient medical report review.<br><br>Not provided if the referral isn’t in the appropriate state or if the patient doesn’t’ require the review. |
| AbsenceRecordKey | string | The key of the absence record the referral is joined to. |
| RejectionReason | string | The reason that the referral was rejected. |
| PublicReasonForReferral | string | The public reason for the referral (public = shared with the employer). |
| DaysToReviewDischargeLetterByPatient | int | The number of days a patient has to review the referral discharge letter |

## JSON Example

```
{

"Key": "R123",

"PatientName": "Mr. John Smith",

"ReferredBy": "Mr. Will Smith",

"CreatedDate": "2015-03-13T14:22:12",

"ModifiedDate": "2015-03-13T14:52:30",

"State": "InProgress",

"StateDisplayName": "In progress",

"StateColor": "green",

"ReferralNumber": 13911,

"AppointmentType": {

"Name": "Referral",

"Key": "REF1",

"Notes": "",

"CanBookAppointment": true,

"CanReferPatient": true

}

"Appointments": \[

{&lt;see AppointmentData&gt;}

\],

"Questionnaires": \[

{

"Key": "q123",

"Name": "Referral",

"Description": "",

"StatusCode": 1,

"Status": "1",

"Expiration": "2015-03-26T14:37:00.2003719+00:00"

}

\],

"Documents": \[

{

"Name": "Referral letter.html",

"Author": "Mr. Will Smith",

"Comment": "I would like to refer Mr. John Smith",

"DateCreated": "2015-03-13T14:22:12.483",

"Url": "<https://api.meddbase.com/referrals/download?d=123>",

"MIMEType": "text/html",

"Size": 20824

}

\],

"CanCancel": false,

"CanBookAppointment": false,

"CanSend": false,

"CanReallocate": true,

"CanCollaborate": true,

"CanAttachDocument": false,

"CanFollowUp": false,

“PatientReview”: {

<see [PatientReportReviewState](#_PatientReportReviewState)\>

},

“AbsenceRecordKey”: “123”,

“RejectionReason”: “Holidays”

“PublicReasonForReferral”: “Angina”,

"DaysToReviewDischargeLetterByPatient": 3

}
```
