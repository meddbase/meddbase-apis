---
layout: page
title: ServiceExceptionData
nav_order: 80
parent: Objects and data types
---

# ServiceExceptionData

Provides information about the exception.

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
            <td>Message</td>
            <td>string</td>
            <td>Message of the exception.</td>
        </tr>
        <tr>
            <td>EventType</td>
            <td>int</td>
            <td>
                <p>Type of the exception:</p>
                <ul>
                    <li>1 = Critical</li>
                    <li>2 = Error</li>
                    <li>4 = Warning</li>
                    <li>8 = Information</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>EventCode</td>
            <td>int</td>
            <td>
                <p>Specific code to identify the exception (argument missing, not logged in, not all required questions
                    of the questionnaire are answered, etc.).</p>
            </td>
        </tr>
        <tr>
            <td>HttpStatusCode</td>
            <td>int</td>
            <td>Same like HTTP status code. See <a href="../error-handling/error-handling">Error handling</a></td>
        </tr>
        <tr>
            <td>Description</td>
            <td>string</td>
            <td>More details of the exception.</td>
        </tr>
        <tr>
            <td>ReferenceNumber</td>
            <td>string</td>
            <td>
                <p>A unique reference number that represents an event in the Meddbase logs. This can be traced by
                    Meddbase support.</p>
            </td>
        </tr>
    </tbody>
</table>

## JSON Example

```json
{
    "Message": "Password isn't set.",
    "EventType": 2,
    "EventCode": 0,
    "HttpStatusCode": 400,
    "Description": null,
    "ReferenceNumber": null
}
```
