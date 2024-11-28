---
layout: page
title: GetTypes
nav_order: 4
parent: Documents
---

# GetTypes

Returns a document types the user may have an access to. The feature needs to be enabled. You could check whether the feature is enabled via GetConfig by checking the DocumentTypeSecurityEnabled flag.

## JavaScript library method

```javascript
patientportal.documents.getTypes();
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/documents/types` |

## Returns

[DocumentType](../objects-and-data-types/documenttype)
