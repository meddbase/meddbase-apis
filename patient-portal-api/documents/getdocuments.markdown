---
layout: page
title: GetDocuments
nav_order: 1
parent: Documents
---

# GetDocuments

Returns the list of document for a specific patient.

## JavaScript library method

```javascript
patientportal.documents.getDocuments({
    patient: <patient>,
    name: <name>,
    createdFrom: <created-from>,
    createdTo: <created-to>,
    pageSortColumn: <page-sort-column>,
    pageSortDescending: <page-sort-descending>,
    pageNumber: <page-number>,
    pageSize: <page-size>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/documents/documents` |

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
            <td>patient</td>
            <td>string</td>
            <td>The key of the patient provided by the API upon GetPatients.</td>
        </tr>
        <tr>
            <td>name</td>
            <td>string (optional)</td>
            <td>Filters the documents by the name.</td>
        </tr>
        <tr>
            <td>created-from</td>
            <td><a href="../objects-and-data-types/datetime">DateTime</a> (optional)</td>
            <td>Filters the documents by the created data.</td>
        </tr>
        <tr>
            <td>created-to</td>
            <td><a href="../objects-and-data-types/datetime">DateTime</a> (optional)</td>
            <td>Filters the documents by the created data.</td>
        </tr>
        <tr>
            <td>page-sort-column</td>
            <td>int (optional)</td>
            <td>
                <p>The column index to sort the result:</p>
                <ul>
                    <li>0 – Name</li>
                    <li>1 – Created date</li>
                </ul>
                <p>Default: 0</p>
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

## Returned JSON

```json
{
    "Items": [
        {
            "Name": "Referral letter.html",
            "Author": "Mr. Will Smith",
            "Comments": "I would like to refer Mr. John Smith",
            "DateCreated": "2015-03-13T14:22:12.483",
            "Url": "https://api.meddbase.com/referrals/download?d=123",
            "MIMEType": "text/html",
            "Size": 20824,
            "PatientKey": "iydksy58dujyhiee78",
            "DocumentTypeName": "Portal Documents"
        }
    ],
    "TotalCount":1,
    "CurrentPage":1,
    "PageSize":10,
    "SortColumn": 0,
    "SortDescending": false
}
```
