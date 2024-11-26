---
layout: page
title: GetPatients
nav_order: 4
parent: Patients
---

# GetPatients

Returns the list of patients. Note that the list includes only patients the logged in user is allowed to view.

## JavaScript library method

```
patientportal.patients.getPatients({

text: &lt;text&gt;,

name: &lt;name&gt;,

surname: &lt;surname&gt;,

department: &lt;department&gt;,

division: &lt;division&gt;,

personalEmail: &lt;personal-email&gt;,

workEmail: &lt;work-email&gt;,

employeeNumber: &lt;employee-number&gt;,

dobFrom: &lt;dob-from&gt;,

dobTo: &lt;dob-to&gt;,

pageSortColumn: &lt;page-sort-column&gt;,

pageSortDescending: &lt;page-sort-descending&gt;,

pageNumber: &lt;page-number&gt;,

pageSize: &lt;page-size&gt;

});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/patients/patients

## URL Parameters

<table><tbody><tr><th><p>text</p></th><th><p>string (optional)</p></th><th><p>Any text the API will try to filter by name, email or employee number.</p></th></tr><tr><td><p>name</p></td><td><p>string (optional)</p></td><td><p>Name filter.</p></td></tr><tr><td><p>surname</p></td><td><p>string (optional)</p></td><td><p>Surname filter.</p></td></tr><tr><td><p>department</p></td><td><p>string (optional)</p></td><td><p>Key of the department provided by the API upon GetDepartments.</p></td></tr><tr><td><p>division</p></td><td><p>string (optional)</p></td><td><p>Key of the division provided by the API upon GetDepartments.</p></td></tr><tr><td><p>personal-email</p></td><td><p>string (optional)</p></td><td><p>Personal email filter.</p></td></tr><tr><td><p>work-email</p></td><td><p>string (optional)</p></td><td><p>Work email filter.</p></td></tr><tr><td><p>employee-number</p></td><td><p>string (optional)</p></td><td><p>Employee number filter.</p></td></tr><tr><td><p>dob-from</p></td><td><p>string (optional)</p></td><td><p>Filter by DOB from. If provided the patients without DOB are filtered out.</p></td></tr><tr><td><p>dob-to</p></td><td><p>string (optional)</p></td><td><p>Filter by DOB to. If provided the patients without DOB are filtered out.</p></td></tr><tr><td><p>page-sort-column</p></td><td><p>int (optional)</p></td><td><p>The column index to sort the result:</p><ul><li>0 – Patient’s name</li><li>1 – Email address</li><li>2 - &lt;ignored&gt;</li><li>3 – Employee number</li></ul><p>By default the result is sorted by the user name.</p></td></tr><tr><td><p>page-sort-descending</p></td><td><p>int (optional)</p></td><td><p>True to sort result descending.</p></td></tr><tr><td><p>page-number</p></td><td><p>int (optional)</p></td><td><p>Required page number. Default 1.</p></td></tr><tr><td><p>page-size</p></td><td><p>int (optional)</p></td><td><p>Required page size. Default 10. Minimum 5. Maximum 50.</p></td></tr></tbody></table>

## Returned JSON

```
{

"Items": \[

&lt;list of PersonDemographicData&gt;

\]

"TotalCount":24,

"CurrentPage":1,

"PageSize":10,

"SortColumn": 0,

"SortDescending": false

}
```
