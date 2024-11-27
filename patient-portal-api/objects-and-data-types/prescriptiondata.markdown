---
layout: page
title: PrescriptionData
nav_order: 65
parent: Objects and data types
---

# PrescriptionData

Contains information about the prescription.

## Properties

<table><tbody><tr><th><p>Key</p></th><th><p>string</p></th><th><p>Key of the prescription.</p></th></tr><tr><td><p>Type</p></td><td><p>string</p></td><td><p>Type of prescription. Possible values are:</p><ul><li>‘R’ (repeat)</li><li>‘A’ (acute)</li></ul></td></tr><tr><td><p>DrugKey</p></td><td><p>string</p></td><td><p>Key of the drug to prescribe.</p></td></tr><tr><td><p>DrugName</p></td><td><p>string</p></td><td><p>Name of the drug to prescribe.</p></td></tr><tr><td><p>Quantity</p></td><td><p>decimal</p></td><td><p>Quantity in a pack.</p></td></tr><tr><td><p>QuantityUnit</p></td><td><p>string</p></td><td><p>Unit of the quantity (e.g. tablets, capsules, etc.).</p></td></tr><tr><td><p>Dosage</p></td><td><p>string</p></td><td><p>How often is the medicine taken (e.g. One to be taken five times a day).</p></td></tr><tr><td><p>Duration</p></td><td><p>int</p></td><td><p>Count of days the medicine is taking.</p></td></tr><tr><td><p>Method</p></td><td><p>string</p></td><td><p>How the medicine is taken (e.g. swallow without chewing, apply liberally, etc.).</p></td></tr><tr><td><p>Route</p></td><td><p>string</p></td><td><p>Route of administration (e.g. Oral Route, Intraocular route, etc.).</p></td></tr><tr><td><p>PharmacyText</p></td><td><p>string</p></td><td><p>Any comments for Pharmacist.</p></td></tr><tr><td><p>LastIssueDate</p></td><td><p>DateTime</p></td><td><p>Last date when this drug was issued.</p></td></tr></tbody></table>

## JSON Example

```json
{
    "Key": "d2546",
    "Type": "R",
    "DrugKey": "d2546",
    "DrugName": "Aspirin Tablets 75 mg",
    "Quantity": 28,
    "QuantityUnit": "tablets",
    "Dosage": "One To Be Taken Each Day",
    "Duration": 28,
    "Method": "",
    "Route": "Oral route",
    "PharmacyText": ""
}
```
