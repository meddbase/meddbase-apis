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

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/users/users` |

## URL Parameters

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
            <td>text</td>
            <td>string (optional)</td>
            <td>Any text the API will try to filter by name, email or employee number.</td>
        </tr>
        <tr>
            <td>name</td>
            <td>string (optional)</td>
            <td>Name filter.</td>
        </tr>
        <tr>
            <td>department</td>
            <td>string (optional)</td>
            <td>Key of the department provided by the API upon GetDepartments.</td>
        </tr>
        <tr>
            <td>division</td>
            <td>string (optional)</td>
            <td>Key of the division provided by the API upon GetDepartments.</td>
        </tr>
        <tr>
            <td>email</td>
            <td>string (optional)</td>
            <td>Email filter.</td>
        </tr>
        <tr>
            <td>employee-number</td>
            <td>string (optional)</td>
            <td>Employee number filter.</td>
        </tr>
        <tr>
            <td>page-sort-column</td>
            <td>int (optional)</td>
            <td>
                <p>The column index to sort the result:</p>
                <ul>
                    <li>0 – User’s name</li>
                    <li>1 – Email address</li>
                    <li>2 – Account type</li>
                    <li>3 – Employee number</li>
                </ul>
                <p>By default the result is sorted by the user name.</p>
            </td>
        </tr>
        <tr>
            <td>page-sort-descending</td>
            <td>int (optional)</td>
            <td>True to sort result descending.</td>
        </tr>
        <tr>
            <td>page-number</td>
            <td>int (optional)</td>
            <td>Required page number. Default 1.</td>
        </tr>
        <tr>
            <td>page-size</td>
            <td>int (optional)</td>
            <td>Required page size. Default 10. Minimum 5. Maximum 50.</td>
        </tr>
    </tbody>
</table>

## Returns

[UserData](../objects-and-data-types/userdata)[]

## Returned JSON

```json
{
    "Items": [
        {
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
            },
            "NextOfKin": {
                "Relationship": "Mam",
                "Name": "Mariel",
                "Surname": "Lemon",
                "Mobile": "+444 895 111 222",
                "WorkTelephone": "+444 525 111 555",
                "Address": {
                    "Address1": "Studio 1",
                    "Address2": "Cardwell Roa",
                    "Address3": "Camden",
                    "City": "London",
                    "County": "",
                    "PostCode": "N1 7NK",
                    "Country": "United Kingdom"
                }
            },
            "AllPatientsVisible": false,
            "AllNonAssignedPatientsVisible": false,
            "Rights": [
                {
                    "Key": "0f0f8997-a161-455e-a498-96138096f539",
                    "Name": "Case management",
                    "Description": "The user can refer patients and manage the referrals."
                }
            ],
            "AccessibleDepartments": [
                {
                    "Key": "D01",
                    "Name": "HR"
                },
                {
                    "Key": "D02",
                    "Name": "Research"
                }
            ],
            "LastLogin": "2015-01-01T10:41:10.547"
        }
    ],
    "TotalCount":1,
    "CurrentPage":1,
    "PageSize":10,
    "SortColumn": 0,
    "SortDescending": false
}
```
