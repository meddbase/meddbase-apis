---
layout: page
title: ServerStateData
nav_order: 78
parent: Objects and data types
---

# ServerStateData

Provides information about an actual server state.

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
            <td>Name</td>
            <td>string</td>
            <td>Name of the server.</td>
        </tr>
        <tr>
            <td>StateCode</td>
            <td>int</td>
            <td>
                <p>Current server state:</p>
                <ul>
                    <li>1 = running</li>
                    <li>2 = updating</li>
                    <li>3 = suspending</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>State</td>
            <td>string</td>
            <td>String representation of the current server state.</td>
        </tr>
        <tr>
            <td>ServiceVersion</td>
            <td>string</td>
            <td>
                <p>Deprecated.</p>
                <p><s>Current version of the server in format: “&lt;major&gt;.&lt;minor&gt;.&lt;build&gt;”. For example:
                        “1.60.2995”.</s></p>
            </td>
        </tr>
        <tr>
            <td>ProtocolVersion</td>
            <td>string</td>
            <td>
                <p>Service communication protocol version in format: “&lt;major&gt;.&lt;minor&gt;.&lt;build&gt;”. For
                    example: “1.0.1”</p>
                <p>The build number can change without the interface changing (adding optional parameters, adding new
                    methods). Change in the major or the minor version means the interface change and the client who
                    doesn’t support new version of interface shouldn’t continue working and needs to be upgraded.</p>
            </td>
        </tr>
    </tbody>
</table>

## JSON Example

```json
{
    "Name": "Meddbase server",
    "StateCode": 1,
    "State": "Running",
    "ServiceVersion": "<deprecated>",
    "ProtocolVersion": "1.0.1"
}
```
