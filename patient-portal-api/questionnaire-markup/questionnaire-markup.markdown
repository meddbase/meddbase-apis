---
layout: page
title: Questionnaire markup
nav_order: 38
parent: Patient Portal API
---

# Questionnaire markup

The questionnaire markup contains the definition of a whole questionnaire: pages, instructions and questions.

## Full questionnaire markup example

```xml
<?xml version="1.0" encoding="utf-8"?>
<Questionnaire>
    <Pages>
        <Page title="Assure - Health Screening Questionnaire">
            <Information>
                Please answer the following questions as far as you can. If in doubt please ask the               doctor later.
            </Information>
            <Field id="314">Job Title</Field>
            <Field required="false" id="315">Department</Field>
            <Information>
                Is there a family history of any of the following (Grandparents, parents, brothers, sisters)?
            </Information>
            <Question id="328">
                <Text>Heart Conditions / Angina</Text>
                <Answers>
                    <Answer>Yes</Answer>
                    <Answer>No</Answer>
                </Answers>
            </Question>
        </Page>
        <Page title="Exercise">
            <Field id="389">What exercise do you do and how often?</Field>
            <Field required="false" id="391">What exercise do you enjoy?</Field>
            <Field required="false" id="392">What exercise do you dislike?</Field>
            <Question required="false" id="394">
                <Text>
                    How active is your job?
                </Text>
                <Answers>
                    <Answer>Light</Answer>
                    <Answer>Moderate</Answer>
                    <Answer>Vigorous</Answer>
                </Answers>
            </Question>
            <Table id="10963" required="false">
                <Text>Occupational History</Text>
                <Column header="Employer" />
                <Column header="Job title" />
                <Column header="From" datatype="date" />
                <Column header="Until" datatype="date" />
            </Table>
        </Page>
    </Pages>
</Questionnaire>
```

## Markup description

Document root `Questionnaire` contains a list of `Pages`.

- The client should can show progress by counting the number of Page tags and using that to show a percentage progress-indicator.

Every `Page` can contain tags:

- `Information` – Plain text that guides the patient and describes/explains the following questions.
- `Field` – Free-text field. The value of this tag contains the field label.
  - The client must use the `id` attribute to submit answers (see SaveQuestionnaire).
  - If the `required` attribute isn't present, then the answer is required. Only if `required="false"` the answer is not required.
- `Question` – question with more answers.
  - The `Text` element contains the question-text.
  - The `Answers` element contains possible answers.
  - The initial state of the UI must be un-set (no answer is selected).
  - Only one answer can be selected.
  - The client must use the `id` attribute to submit answer (see SaveQuestionnaire).
  - If the `required` attribute isn't present, then the answer is required. Only if `required="false"` the answer is not required.
