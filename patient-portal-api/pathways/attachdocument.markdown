---
layout: page
title: AttachDocument
nav_order: 7
parent: Pathways
---

# AttachDocument

Attaches a document to a pathway task.

## JavaScript library method

```
patientportal.pathways.attachDocument({

pathway: &lt;pathway&gt;,

task: &lt;task&gt;,

documentName: &lt;document-name&gt;,

documentComments: &lt;document-comments&gt;,

uploading: {

file: &lt;file&gt;,

onProgress: &lt;onProgress&gt;,

}

});
```

## HTTP Method

POST

## ****Url****

/patientportalapi/pathways/attach-document

## URL Parameters

| pathway | string | Pathway key |
| --- | --- | --- |
| task | string | Task key |
| document-name | string | The name of the document. |
| document-comments | string (optional) | The document comments/description. |
| uploading.file | javascript:<br><br>File | File instance provided by JavaScript input element:<br><br>file:document.getElementById("myFile").files\[0\] |
| uploading.onProgress | javascript :<br><br>function (int) | Progress callback. For example:<br><br>onProgress: function (progress) {<br><br>console.log("Progress: " +<br><br>progress + "% uploaded."); <br><br>} |

## Returns

PathwayData

## Remarks

Please note the body of the request is the actual document content. For that reason you need to include ASP.NET_SessionId in cookies and the token in URL.
