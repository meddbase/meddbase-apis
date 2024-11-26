---
layout: page
title: ManagerReportReviewData
nav_order: 45
parent: Objects and data types
---

# ManagerReportReviewData

Provides information about the manager review.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| ReportUrl | string | The URL address of the full medical report. The report is PDF document.<br><br>We recommend to use &lt;object&gt; tag to display embedded PDF:<br><br>&lt;object type="application/pdf" data="<url&gt;">&lt;/object&gt; |
| ReferredBy | string | The name of the referrer. |
| Referral | ReferralData | The referral data. |

## JSON Example

```
{

"ReportUrl": "<http://api.meddbase.com/patientportalapi/>....",

"ReferredBy": "Mr. John Smith",

"Referral": {&lt;...see ReferralData...&gt;},

}
```
