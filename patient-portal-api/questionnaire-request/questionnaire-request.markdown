---
layout: page
title: Questionnaire Request
nav_order: 25
parent: Patient Portal API
---

# Questionnaire Request


This section provides methods for a patient to complete a questionnaire without having to register with the portal or use a password. The client has to provide the client key only (see Client authentication).

Workflow: The patient gets the email which includes URL address to the online portal and the validation key (URL get parameter). The client needs to provide validation key within each request in this section.

The process goes through these steps:

- Validation process through email or phone
- Save questionnaire (they are allowed to come back later)
- Submit questionnaire
