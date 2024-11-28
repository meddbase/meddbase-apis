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

<table><tbody><tr><th><p>patient</p></th><th><p>string</p></th><th><p>The key of the patient provided by the API upon GetPatients.</p></th></tr><tr><td><p>name</p></td><td><p>string (optional)</p></td><td><p>Filters the documents by the name.</p></td></tr><tr><td><p>created-from</p></td><td><p>DateTime (optional)</p></td><td><p>Filters the documents by the created data.</p></td></tr><tr><td><p>created-to</p></td><td><p>DateTime (optional)</p></td><td><p>Filters the documents by the created data.</p></td></tr><tr><td><p>page-sort-column</p></td><td><p>int (optional)</p></td><td><p>The column index to sort the result:</p><ul><li>0 – Name</li><li>1 – Created date</li></ul><p>Default: 0</p></td></tr><tr><td><p>page-sort-descending</p></td><td><p>int (optional)</p></td><td><p>True to sort result descending.</p></td></tr><tr><td><p>page-number</p></td><td><p>int (optional)</p></td><td><p>Required page number. Default 1.</p></td></tr><tr><td><p>page-size</p></td><td><p>int (optional)</p></td><td><p>Required page size. Default 10. Minimum 5. Maximum 50.</p></td></tr></tbody></table>

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
