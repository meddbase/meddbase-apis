---
layout: page
title: GetReferrals
nav_order: 1
parent: Referrals
---

# GetReferrals

Returns the referrals that meets the search criteria.

## JavaScript library method

```
patientportal.referrals.getReferrals({

patient: &lt;patient&gt;,

text: &lt;text&gt;,

status: &lt;status&gt;,

referralNumber: &lt;referral-number&gt;,

patientName: &lt;patient-name&gt;,

referrerName: &lt;referrer-name&gt;,

department: &lt;department&gt;,

division: &lt;division&gt;,

case: &lt;case&gt;,

pageSortColumn: &lt;page-sort-column&gt;,

pageSortDescending: &lt;page-sort-descending&gt;,

pageNumber: &lt;page-number&gt;,

pageSize: &lt;page-size&gt;

});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/referrals/referrals

## URL Parameters

<table><tbody><tr><th><p>patient</p></th><th><p>string (optional)</p></th><th><p>The key of the patient provided by the API upon GetPatients.</p></th></tr><tr><td><p>text</p></td><td><p>string (optional)</p></td><td><p>Any text the API will try to filter by patient’s/referrer’s name, email, employee number or by referral number if the text is a number.</p></td></tr><tr><td><p>status</p></td><td><p>int (optional)</p></td><td><p>Status filter:</p><ul><li>0 – &lt;disabled, filter no active&gt;</li><li>1 – Questionnaire required</li><li>2 – Documents required</li><li>3 – In progress</li><li>4 – Closed only</li><li>5 – Opened only</li></ul></td></tr><tr><td><p>referral-number</p></td><td><p>string (optional)</p></td><td><p>The number of the referral.</p></td></tr><tr><td><p>patient-name</p></td><td><p>string (optional)</p></td><td><p>The patient name.</p></td></tr><tr><td><p>referrer-name</p></td><td><p>string (optional)</p></td><td><p>The referrer name.</p></td></tr><tr><td><p>department</p></td><td><p>string (optional)</p></td><td><p>Key of the department provided by the API upon GetDepartments.</p></td></tr><tr><td><p>division</p></td><td><p>string (optional)</p></td><td><p>Key of the division provided by the API upon GetDepartments.</p></td></tr><tr><td><p>case</p></td><td><p>int (optional)</p></td><td><p>The case key for the referral.</p></td></tr><tr><td><p>page-sort-column</p></td><td><p>int (optional)</p></td><td><p>The column index to sort the result:</p><ul><li>0 – Last modification date</li><li>1 – Referral number</li><li>2 – Patient name</li><li>3 – Referrer name</li><li>4 – Date created</li></ul><p>By default the result is sorted by last modification date.</p></td></tr><tr><td><p>page-sort-descending</p></td><td><p>int (optional)</p></td><td><p>True to sort result descending. Note that this parameter is ignored for column index 0.</p></td></tr><tr><td><p>page-number</p></td><td><p>int (optional)</p></td><td><p>Required page number. Default 1.</p></td></tr><tr><td><p>page-size</p></td><td><p>int (optional)</p></td><td><p>Required page size. Default 10. Minimum 5. Maximum 50.</p></td></tr></tbody></table>

## Returned JSON

```
{

"Items": \[

&lt;list of ReferralOverviewData&gt;

\]

"TotalCount":24,

"CurrentPage":1,

"PageSize":10,

"SortColumn": 0,

"SortDescending": false

}
```
