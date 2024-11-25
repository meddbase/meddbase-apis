---
layout: page
title: GetUsers
nav_order: 5
parent: Users
---

# GetUsers

Returns the list of users.

## JavaScript library method

```javascript
patientportal.users.getUsers({
    text: <text>,
    name: <name>,
    department: <department>,
    division: <division>,
    email: <email>,
    employeeNumber: <employee-number>,
    pageSortColumn: <page-sort-column>,
    pageSortDescending: <page-sort-descending>,
    pageNumber: <page-number>,
    pageSize: <page-size>
});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/users/users

## URL Parameters

<table><tbody><tr><th><p>text</p></th><th><p>string (optional)</p></th><th><p>Any text the API will try to filter by name, email or employee number.</p></th></tr><tr><td><p>name</p></td><td><p>string (optional)</p></td><td><p>Name filter.</p></td></tr><tr><td><p>department</p></td><td><p>string (optional)</p></td><td><p>Key of the department provided by the API upon GetDepartments.</p></td></tr><tr><td><p>division</p></td><td><p>string (optional)</p></td><td><p>Key of the division provided by the API upon GetDepartments.</p></td></tr><tr><td><p>email</p></td><td><p>string (optional)</p></td><td><p>Email filter.</p></td></tr><tr><td><p>employee-number</p></td><td><p>string (optional)</p></td><td><p>Employee number filter.</p></td></tr><tr><td><p>page-sort-column</p></td><td><p>int (optional)</p></td><td><p>The column index to sort the result:</p><ul><li>0 – User’s name</li><li>1 – Email address</li><li>2 – Account type</li><li>3 – Employee number</li></ul><p>By default the result is sorted by the user name.</p></td></tr><tr><td><p>page-sort-descending</p></td><td><p>int (optional)</p></td><td><p>True to sort result descending.</p></td></tr><tr><td><p>page-number</p></td><td><p>int (optional)</p></td><td><p>Required page number. Default 1.</p></td></tr><tr><td><p>page-size</p></td><td><p>int (optional)</p></td><td><p>Required page size. Default 10. Minimum 5. Maximum 50.</p></td></tr></tbody></table>

## Returned JSON

```
{

"Items": \[

<list of UserData>

\]

"TotalCount":24,

"CurrentPage":1,

"PageSize":10,

"SortColumn": 0,

"SortDescending": false

}
```
