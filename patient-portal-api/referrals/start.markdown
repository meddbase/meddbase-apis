---
layout: page
title: Start
nav_order: 3
parent: Referrals
---

# Start

Starts and returns a new referral.

## JavaScript library method

```javascript
patientportal.referrals.start({
    patient: <patient>,
    appointmentType: <appointment-type>,
    caseTitle: <case-title>
});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/referrals/start` |

## URL Parameters

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| patient | string | The key of the patient provided by the API upon section Patients. |
| appointmentType | string | The key of the appointment type provided by the API upon GetAppointmentTypes. To find out how to work with referral appointments please read section **Error! Reference source not found.**. |
| caseTitle | string | The reason for starting the referral. |

## Returns

ReferralData
