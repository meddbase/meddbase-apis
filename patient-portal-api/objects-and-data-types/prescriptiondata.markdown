---
layout: page
title: PrescriptionData
nav_order: 65
parent: Objects and data types
---

# PrescriptionData

Contains information about the prescription.

## Properties

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
            <td>Key</td>
            <td>string</td>
            <td>Key of the prescription.</td>
        </tr>
        <tr>
            <td>Type</td>
            <td>string</td>
            <td>
                <p>Type of prescription. Possible values are:</p>
                <ul>
                    <li>‘R’ (repeat)</li>
                    <li>‘A’ (acute)</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>DrugKey</td>
            <td>string</td>
            <td>Key of the drug to prescribe.</td>
        </tr>
        <tr>
            <td>DrugName</td>
            <td>string</td>
            <td>Name of the drug to prescribe.</td>
        </tr>
        <tr>
            <td>Quantity</td>
            <td>decimal</td>
            <td>Quantity in a pack.</td>
        </tr>
        <tr>
            <td>QuantityUnit</td>
            <td>string</td>
            <td>Unit of the quantity (e.g. tablets, capsules, etc.).</td>
        </tr>
        <tr>
            <td>Dosage</td>
            <td>string</td>
            <td>How often is the medicine taken (e.g. One to be taken five times a day).</td>
        </tr>
        <tr>
            <td>Duration</td>
            <td>int</td>
            <td>Count of days the medicine is taking.</td>
        </tr>
        <tr>
            <td>Method</td>
            <td>string</td>
            <td>How the medicine is taken (e.g. swallow without chewing, apply liberally, etc.).</td>
        </tr>
        <tr>
            <td>Route</td>
            <td>string</td>
            <td>Route of administration (e.g. Oral Route, Intraocular route, etc.).</td>
        </tr>
        <tr>
            <td>PharmacyText</td>
            <td>string</td>
            <td>Any comments for Pharmacist.</td>
        </tr>
        <tr>
            <td>LastIssueDate</td>
            <td><a href="../objects-and-data-types/datetime">DateTime</a></td>
            <td>Last date when this drug was issued.</td>
        </tr>
    </tbody>
</table>

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
