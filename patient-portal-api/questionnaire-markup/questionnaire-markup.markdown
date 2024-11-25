---
layout: page
title: Questionnaire markup
nav_order: 38
parent: Patient Portal API
---

# Questionnaire markup


The questionnaire markup contains the definition of a whole questionnaire: pages, instructions and questions.

#### Full questionnaire markup example

```
&lt;?xml version="1.0" encoding="utf-8"?&gt;

&lt;Questionnaire&gt;

&lt;Pages&gt;

&lt;Page title="Assure - Health Screening Questionnaire"&gt;

&lt;Information&gt;

Please answer the following questions as far as you can. If in doubt please ask the doctor later.

&lt;/Information&gt;

&lt;Field id="314"&gt;Job Title&lt;/Field&gt;

&lt;Field required="false" id="315"&gt;Department&lt;/Field&gt;

&lt;Information&gt;

Is there a family history of any of the following (Grandparents, parents, brothers, sisters)?

&lt;/Information&gt;

&lt;Question id="328"&gt;

&lt;Text&gt;Heart Conditions / Angina&lt;/Text&gt;

&lt;Answers&gt;

&lt;Answer&gt;Yes&lt;/Answer&gt;

&lt;Answer&gt;No&lt;/Answer&gt;

&lt;/Answers&gt;

&lt;/Question&gt;

&lt;/Page&gt;

&lt;Page title="Exercise"&gt;

&lt;Field id="389"&gt;What exercise do you do and how often?&lt;/Field&gt;

&lt;Field required="false" id="391"&gt;What exercise do you enjoy?&lt;/Field&gt;

&lt;Field required="false" id="392"&gt;What exercise do you dislike?&lt;/Field&gt;

&lt;Question required="false" id="394"&gt;

&lt;Text&gt;

How active is your job?

&lt;/Text&gt;

&lt;Answers&gt;

&lt;Answer&gt;Light&lt;/Answer&gt;

&lt;Answer&gt;Moderate&lt;/Answer&gt;

&lt;Answer&gt;Vigorous&lt;/Answer&gt;

&lt;/Answers&gt;

&lt;/Question&gt;

&lt;Table id="10963" required="false"&gt;

&lt;Text&gt;Occupational History&lt;/Text&gt;

&lt;Column header="Employer" /&gt;

&lt;Column header="Job title" /&gt;

&lt;Column header="From" datatype="date" /&gt;

&lt;Column header="Until" datatype="date" /&gt;

&lt;/Table&gt;

&lt;/Page&gt;

&lt;/Pages&gt;

&lt;/Questionnaire&gt;
```

#### Markup description

Document root Questionnaire contains a list of Pages.

- The client should can show progress by counting the number of Page tags and using that to show a percentage progress-indicator.

Every Page can contain tags:

- Information – Plain text that guides the patient and describes/explains the following questions.
- Field – Free-text field. The value of this tag contains the field label.
  - The client must use the id attribute to submit answers (see SaveQuestionnaire).
  - If the required attribute isn't present, then the answer is required. Only if required="false" the answer is not required.
- Question – question with more answers.
  - The Text element contains the question-text.
  - The Answers element contains possible answers.
  - The initial state of the UI must be un-set (no answer is selected).
  - Only one answer can be selected.
  - The client must use the id attribute to submit answer (see SaveQuestionnaire).
  - If the required attribute isn't present, then the answer is required. Only if required="false" the answer is not required.
