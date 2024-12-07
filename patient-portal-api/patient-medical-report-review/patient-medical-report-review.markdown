---
layout: page
title: Patient Medical Report Review
nav_order: 21
parent: Patient Portal API
---

# Patient Medical Report Review

This section provides methods to manage patient’s review of the medical report for the patient. The patient doesn’t need to be logged in. The client has to provide the client key only (see [Client authentication](../communication-overview/client-authentication)).

Workflow: The patient gets the email which includes URL address to the online portal and the validation key (URL get parameter). The client needs to provide validation key within each request in this section.

Obvious reviewing process goes through those steps:

- Validation process through email or phone
- Reviewing
- Releasing or refusing the report with/without factual changes or comments
