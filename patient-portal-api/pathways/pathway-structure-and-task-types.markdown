---
layout: page
title: Pathway structure and task types
nav_order: 1
parent: Pathways
---

# Pathway structure and task types

The pathway is a set of nested tasks. A task could be either a simple action or a container (either serial or parallel). Containers include other nested tasks. An example of a pathway is provided here PathwayData. Below is the list of action types you can receive via API.

| **Type** | **Name** | **Description** |
| --- | --- | --- |
| WF  | Workflow | The workflow is a container of tasks that runs in order. The workflow is a logical unit like ‘Book first consultation’ that than includes more task like attach document, book an appointment, pre-appointment questionnaire and arrive appointment. |
| SQ  | Sequence | The sequence is a container of tasks that runs in order like the workflow but does not represent a big standalone unit like a workflow. The sequence is used for small sequence tasks within a workflow. |
| ST  | Step | A container of parallel tasks. |
| PL  | Parallel | A container of parallel tasks. |
| BA  | Book an appointment | The task to book an appointment. The task provides the appointment type and optional services that are required to be booked. To book the appointment see Appointments section. |
| AA  | Arrive an appointment | The purpose of this task is to wait for the appointment. However if the booked appointment has been cancelled in the meantime the IsBooked field of AppointmentTaskData is false and the patient needs to book an appointment again in the same way as with the Book an appointment task. |
| QR  | Questionnaire | The patient questionnaire to complete. Use Key field from QuestionnaireTaskData to get the questionnaire details and complete the questionnaire (see GetQuestionnaireDetail). |
| AD  | Attach document | A task to attach a document. The document can be attached via AttachDocument API method. |
| GT  | General task | The general task provides some text (task Description) that needs to be accepted via GetTask API metnod. |
| CH  | Choice<br><br>_(Make a decision pathway task)_ | The choice provides a different list of options and the patient needs to choose one of them. You can submit the selected option via ChooseOption API method. |
