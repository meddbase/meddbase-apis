---
layout: page
title: UpdateDemographicData
nav_order: 4
parent: Patient
---

# UpdateDemographicData

Update the patient’s demographic data.

## JavaScript library method

```javascript
patientportal.patient.updateDemographicData({password: <password>, demog: <demog>});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| POST | `/patientportalapi/patient/demographic-data` |

## POST Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| password | string | Patient’s plain text password to authenticate the patient. |
| demog | PersonDemographicData | Patient’s demographic data to update. If any property is empty (“”), it will be updated. If any property is null (or not defined), it will not be updated. |

## POST data example

```
{

"password": "pass123",

"demog": {

"Title": "Mr",

"Name": "John",

"Surname": "Lemon",

"DateOfBirth": "1958-08-02T00:00:00",

"EmailAddress": "<john.lemon@test.com>",

"Telephone": ""

}

}
```

In the example above only properties Title, Name, Surname, DataOfBirth, EmailAddress and Telephone will update. All another properties will not be changed because they are not in POST data.
