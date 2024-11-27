---
layout: page
title: PathwayTaskOverviewData
nav_order: 53
parent: Objects and data types
---

# PathwayTaskOverviewData

An overview of a single task within a pathway.

## Properties

<table><tbody><tr><th colspan="2"><p>Key</p></th><th colspan="2"><p>string</p></th><th><p>The key of the task.</p></th></tr><tr><td colspan="2"><p>Name</p></td><td colspan="2"><p>string</p></td><td><p>The name of the task.</p></td></tr><tr><td colspan="2"><p>ActionType</p></td><td colspan="2"><p>string</p></td><td><p>The type of the task. See Pathway structure and task types.</p></td></tr><tr><td colspan="2"><p>ActionTypeName</p></td><td colspan="2"><p>string</p></td><td><p>The user-friendly name of the action type.</p></td></tr><tr><td colspan="2"><p>StateType</p></td><td colspan="2"><p>string</p></td><td><p>The state of the task.</p><ul><li>FT – Future pending task, not-started yet</li><li>ST – Started task</li><li>IP – Task in progress</li><li>CP – Task completed</li><li>SK – Task has been skipped</li><li>FL – Task failed</li></ul><p>Note that even if the task is in ST (Started) state the client need to check CanProcess field to allow any action.</p></td></tr><tr><td colspan="2"><p>StateName</p></td><td colspan="2"><p>string</p></td><td><p>The user-friendly name of the state.</p></td></tr><tr><td colspan="2"><p>CanProcess</p></td><td colspan="2"><p>bool</p></td><td><p>True if the task and the logged-in user has rights to process the task.</p></td></tr><tr><td><p>Tasks</p></td><td colspan="2"><p>PathwayTaskOverviewData[]</p></td><td colspan="2"><p>The list of nested tasks.</p></td></tr></tbody></table>

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
