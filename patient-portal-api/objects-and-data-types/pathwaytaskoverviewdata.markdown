---
layout: page
title: PathwayTaskOverviewData
nav_order: 53
parent: Objects and data types
---

# PathwayTaskOverviewData

An overview of a single task within a pathway.

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
            <td>The key of the task.</td>
        </tr>
        <tr>
            <td>Name</td>
            <td>string</td>
            <td>The name of the task.</td>
        </tr>
        <tr>
            <td>ActionType</td>
            <td>string</td>
            <td>The type of the task. See <a href="../pathways/pathway-structure-and-task-types">Pathway structure and task types</a>.</td>
        </tr>
        <tr>
            <td>ActionTypeName</td>
            <td>string</td>
            <td>The user-friendly name of the action type.</td>
        </tr>
        <tr>
            <td>StateType</td>
            <td>string</td>
            <td>
                <p>The state of the task.</p>
                <ul>
                    <li>FT – Future pending task, not-started yet</li>
                    <li>ST – Started task</li>
                    <li>IP – Task in progress</li>
                    <li>CP – Task completed</li>
                    <li>SK – Task has been skipped</li>
                    <li>FL – Task failed</li>
                </ul>
                <p>Note that even if the task is in ST (Started) state the client need to check CanProcess field to
                    allow any action.</p>
            </td>
        </tr>
        <tr>
            <td>StateName</td>
            <td>string</td>
            <td>The user-friendly name of the state.</td>
        </tr>
        <tr>
            <td>CanProcess</td>
            <td>bool</td>
            <td>True if the task and the logged-in user has rights to process the task.</td>
        </tr>
        <tr>
            <td>Tasks</td>
            <td><a href="../objects-and-data-types/pathwaytaskoverviewdata">PathwayTaskOverviewData</a>[]</td>
            <td>The list of nested tasks.</td>
        </tr>
    </tbody>
</table>

## JSON Example

```json
{
    "Name": "AA",
    "ActionType": "AA",
    "ActionTypeName": "Arrive an appointment",
    "StateType": "FT",
    "StateName": "Future task",
    "CanProcess": false,
    "Key": "86149d568252ae476859a3a60835369b"
}
```
