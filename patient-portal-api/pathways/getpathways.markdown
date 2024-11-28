---
layout: page
title: GetPathways
nav_order: 2
parent: Pathways
---

# GetPathways

Returns the list of pathways shared with the currently logged-in patient.

## JavaScript library method

```javascript
patientportal.pathways.getPathways({
    pageSortColumn: <page-sort-column>,
    pageSortDescending: <page-sort-descending>,
    pageNumber: <page-number>,
    pageSize: <page-size>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/pathways/pathways` |

## URL Parameters

<table><tbody><tr><th><p>page-sort-column</p></th><th><p>int (optional)</p></th><th><p>The column index to sort the result:</p><ul><li>0 – Last modified</li><li>1 – Pathway ID</li><li>3 – Due date</li><li>4 – Pathway name</li></ul><p>Default: 0</p></th></tr><tr><td><p>page-sort-descending</p></td><td><p>int (optional)</p></td><td><p>True to sort result descending.</p></td></tr><tr><td><p>page-number</p></td><td><p>int (optional)</p></td><td><p>Page number. Default 1.</p></td></tr><tr><td><p>page-size</p></td><td><p>int (optional)</p></td><td><p>Page size. Default 10. Minimum 5. Maximum 50.</p></td></tr></tbody></table>

## Returns

[PathwayOverviewData](../objects-and-data-types/pathwayoverviewdata)[]

## Returned JSON

```json
{
    "Items": [
        {
            "Key": "a1d3e2d1",
            "Number": "123",
            "Name": "Book & Arrive",
            "Patient": "Mr. Will Smith",
            "State": "In progress",
            "CurrentAction": "Book an appointment",
            "LastUpdate": "2015-03-13T14:22:12",
            "DueDate": "2015-03-13T14:52:30"
        }
    ],
    "TotalCount":1,
    "CurrentPage":1,
    "PageSize":10
}
```
