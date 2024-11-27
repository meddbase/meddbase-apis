---
layout: page
title: PatientReportReviewData
nav_order: 59
parent: Objects and data types
---

# PatientReportReviewData

Provides information about the patient medical report review for the patient.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| ReportUrl | string | The URL address of the full medical report. The report is PDF document.<br><br>We recommend to use &lt;object&gt; tag to display embedded PDF:<br><br>&lt;object type="application/pdf" data="<url&gt;">&lt;/object&gt; |
| ReferredBy | string | The name of the referrer. |
| AutoReleaseTime | DateTime | Defines the time when the automatic release is scheduled. |
| PossibleFactualChanges | string[] | List of possible factual changes the patient can request. |
| Submitted | bool | Defines whether the review has already been submitted. It is not allowed to submit the review more than once. |
| Comments | string | The comments provided by the patient for the referrer.<br><br>Provided only if the Submitted==true |
| FactualChanges | object[]<br><br>see example | The list of factual changes requested by the patient.<br><br>Provided only if the Submitted==true |

## JSON Example

```
{

"ReportUrl": "<http://api.meddbase.com/patientportalapi/>....",

"ReferredBy": "Mr. John Smith",

"AutoReleaseTime": "2015-05-14T06:00:00",

"PossibleFactualChanges": \[

"DOB incorrect",

"Name incorrect",

"other"

\],

"Submitted": false,

"Comments": "&lt;Patient’s previous comments if submitted&gt;",

"FactualChanges": \[

{

"Subject": "DOB incorrect",

"Comments": "My DOB is 1.1.1985"

},

{...}

\]

}
```
