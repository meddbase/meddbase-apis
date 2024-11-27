---
layout: page
title: AttachDocument
nav_order: 5
parent: Referrals
---

# AttachDocument

Uploads and attaches a new document to the existing referral.

## JavaScript library method

```javascript
patientportal.referrals.attachDocument({
    referral: <referral>,
    documentName: <document-name>,
    documentComments: <document-comments>,
    uploading: {
        file: <file>,
        onProgress: <onProgress>,
    }
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/referrals/attach-document` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| referral | string | The key of the referral provided by the API upon GetReferrals. |
| document-name | string | The name of the document. |
| document-comments | string (optional) | The document comments/description. |
| uploading.file | javascript:<br><br>File | File instance provided by JavaScript input element:<br><br>file:document.getElementById("myFile").files\[0\] |
| uploading.onProgress | javascript :<br><br>function (int) | Progress callback. For example:<br><br>onProgress: function (progress) {<br><br>console.log("Progress: " +<br><br>progress + "% uploaded."); <br><br>} |

## Returns

[ReferralData](../objects-and-data-types/referraldata)

## Remarks

Please note the body of the request is the actual document content. For that reason you need to include ASP.NET_SessionId in cookies and the token in URL.
