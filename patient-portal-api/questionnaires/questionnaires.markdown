---
layout: page
title: Questionnaires
nav_order: 24
parent: Patient Portal API
---

# Questionnaires

This section provides the ability to work with explicitly requested patient questionnaires (as opposed to questionnaires linked to appointments). Only a logged in user with the `CanViewPatient` right can use this section. Specific rights are also required for individual methods as well.

Note that all the methods which take a ‘category’ parameter only accept the category ‘ppq’. Other categories may be supported in the future.
