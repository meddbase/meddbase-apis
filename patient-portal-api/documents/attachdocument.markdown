---
layout: page
title: AttachDocument
nav_order: 2
parent: Documents
---

# AttachDocument

Uploads and attaches a new document to the patient’s records.

## JavaScript library method

```javascript
patientportal.documents.attachDocument({
    patient: <patient>,
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
| POST | `/patientportalapi/documents/attach` |

## URL Parameters

| patient | string | The key of the patient provided by the API upon GetPatients. |
| --- | --- | --- |
| document-name | string | The name of the document. |
| document-comments | string (optional) | The document comments/description. |
| uploading.file | javascript:<br><br>File | File instance provided by JavaScript input element:<br><br>file:document.getElementById("myFile").files\[0\] |
| uploading.onProgress | javascript :<br><br>function (int) | Progress callback. For example:<br><br>onProgress: function (progress) {<br><br>console.log("Progress: " +<br><br>progress + "% uploaded."); <br><br>} |

## Returns

DocumentData

## Remarks

Please note the body of the request is the actual document content. For that reason you need to include ASP.NET_SessionId in cookies and the token in URL.
