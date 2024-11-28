---
layout: page
title: PathwayTaskData
nav_order: 52
parent: Objects and data types
---

# PathwayTaskData

A full task description within a pathway.

## Properties

<table><tbody><tr><th><p>Key</p></th><th><p>string</p></th><th><p>The key of the task.</p></th></tr><tr><td><p>Name</p></td><td><p>string</p></td><td><p>The name of the task.</p></td></tr><tr><td><p>ActionType</p></td><td><p>string</p></td><td><p>The type of the task. See Pathway structure and task types.</p></td></tr><tr><td><p>ActionTypeName</p></td><td><p>string</p></td><td><p>The user-friendly name of the action type.</p></td></tr><tr><td><p>Description</p></td><td><p>string</p></td><td><p>The description of the task.</p></td></tr><tr><td><p>StateType</p></td><td><p>string</p></td><td><p>The state of the task.</p><ul><li>FT – Future pending task, not-started yet</li><li>ST – Started task</li><li>IP – Task in progress</li><li>CP – Task completed</li><li>SK – Task has been skipped</li><li>FL – Task failed</li></ul><p>Note that even if the task is in ST (Started) state the client need to check CanProcess field to allow any action.</p></td></tr><tr><td><p>StateName</p></td><td><p>string</p></td><td><p>The user-friendly name of the state.</p></td></tr><tr><td><p>CanProcess</p></td><td><p>bool</p></td><td><p>True if the task and the logged-in user has rights to process the task.</p></td></tr><tr><td><p>AppointmentTask</p></td><td><p>AppointmentTaskData</p></td><td><p>The details about the book/arrive appointment task.</p></td></tr><tr><td><p>AttachDocumentTask</p></td><td><p>AttachDocumentTaskData</p></td><td><p>The details about the attach document task.</p></td></tr><tr><td><p>ChoiceTask</p></td><td><p>ChoiceTaskData</p></td><td><p>The details about the choice task.</p></td></tr><tr><td><p>QuestionnaireTask</p></td><td><p>QuestionnaireTaskData</p></td><td><p>The details about the questionnaire task.</p></td></tr></tbody></table>

## JSON Example

```json
{
    "Name": "AA",
    "ActionType": "AA",
    "ActionTypeName": "Arrive an appointment",
    "Description": "Please arrive to your appointment.",
    "StateType": "FT",
    "StateName": "Future task",
    "CanProcess": false,
    "AppointmentTask": {
        "AppointmentType": "0001a9748715e6a2",
        "AppointmentTypeName": "Consultation",
        "IsBooked": false
    },
    "Key": "86149d568252ae476859a3a60835369b"
}
```
