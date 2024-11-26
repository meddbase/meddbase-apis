---
layout: page
title: DocumentData
nav_order: 30
parent: Objects and data types
---

# DocumentData

Provides information about the document.

## Properties

| Name | string | The name of the document. |
| --- | --- | --- |
| Author | User | The type of the user account. |
| Comments | string | Short description or comment. |
| DateCreated | DateTime | Created date. |
| Url | string | Url to download the document. |
| MIMEType | string | MIME type of the document. |
| Size | long | Size in bytes. Can be null. |
| PatientKey | String | The key of the patient. |
| DocumentTypeName | String | The name of the document type the document belongs to.<br><br>Provided only if the DocumentTypeSecurityEnable flag is set (see GetConfig) |

## JSON Example

```
{

"Name": "Referral letter.html",

"Author": "Mr. Will Smith",

"Comments": "I would like to refer Mr. John Smith",

"DateCreated": "2015-03-13T14:22:12.483",

"Url": "<https://api.meddbase.com/referrals/download?d=123>",

"MIMEType": "text/html",

"Size": 20824,

"PatientKey": "iydksy58dujyhiee78",

"DocumentTypeName": "Portal Documents"

}
```
