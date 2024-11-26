---
layout: page
title: GetMedicalHistoryTreeNode
nav_order: 1
parent: Medical history
---

# GetMedicalHistoryTreeNode

Return node from the Medical History tree. To understand how to read the patient’s medical history read chapter Reading the Medical History tree.

## JavaScript library method

```javascript
patientportal.medicalHistory.getMedicalHistoryTreeNode({
    nodePath: <node-path>,
    sendByEmail: <send-by-email>
});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/medical-history/node/&lt;node-path&gt;

## URL node path

| node-path | string | The path of the node provided by the API upon GetMedicalHistoryTreeNode. If the path is specific the requested node is always fully loaded. If the path is empty the server returns root node.<br><br>This parameter is not a query parameter. It is a part of the URL path.<br><br>For example: The URL for the node ‘numeric-data/weight’:<br><br>/patientportalapi/medical-history/node/numeric-data/weight |
| --- | --- | --- |

## URL parameters

| send-by-email | bool (optional) | If true the server sends the specific medical history item to the patient’s email address.<br><br>The client should show a warning message that sending medical information over email isn't encrypted and that the patient should use this feature at their own risk.<br><br>For example: The URL for the node ‘numeric-data/weight’ where the client wants to send the medical history item to the patient’s email address:<br><br>/patientportalapi/medical-history/node/numeric-data/weight?send-by-email=true |
| --- | --- | --- |

## Returns

MedicalHistoryNodeData

## Remarks

If the specific node doesn’t exist the client gets exception where event code is 50001. The client should go back to the parent node.
