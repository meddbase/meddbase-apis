---
layout: page
title: DocumentType
nav_order: 31
parent: Objects and data types
---

# DocumentTypeProvides information about the document type.## Properties| Key | string | The key of the document type. || --- | --- | --- || Name | string | The name of the document type. || AlwaysAccessible | bool | True if the type is built-in and always accessible. This is usually ‘Portal Documents’ because it is used for uploading and all managers has to have access to that type.<br><br>Note this applies if the DocumentTypeSecurityEnable flag is set (see GetConfig) |## JSON Example```{"Key": "22c45458525be86005e08d219b79c5d7","Author": "Portal Documents","AlwaysAccessible": true}```