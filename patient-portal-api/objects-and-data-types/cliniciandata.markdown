---
layout: page
title: ClinicianData
nav_order: 19
parent: Objects and data types
---

# ClinicianData

Information about the clinician.

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
            <td>int</td>
            <td></td>
        </tr>
        <tr>
            <td>SexType</td>
            <td>string</td>
            <td>
                <p>Sex:</p>
                <ul>
                    <li>0 = any</li>
                    <li>1 = male</li>
                    <li>2 = female</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>FullName</td>
            <td>string</td>
            <td></td>
        </tr>
    </tbody>
</table>

## JSON Example

```json
{
    "Key": 84,
    "FullName": "Dr. House"
}
```
