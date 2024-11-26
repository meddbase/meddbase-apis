---
layout: page
title: Authorise
nav_order: 1
parent: Telemedicine
---

# Authorise

Authorises the key and returns the token for the client app to connect to the video.

## JavaScript library method

```javascript
patientportal.telemedicine.authorise({key: <key>});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/telemedicine/authorise` |

## URL Parameters

| key | string | Key to verify and generate token against. This key is part of the URL provided to access telemedicine conference. |
| --- | --- | --- |
| username | string | The name of the participant. |

## Returns

AuthorizeTelemedicineData

## Remarks

Authorises the user’s access to telemedicine conference and returns the token that could be used to lunch the video app.

## Twilio integration

Currently the Meddbase application supports [Twilio](https://www.twilio.com/) provider only. Twilio provides a multi-party video application to demonstrate how you could built a solution with [Twilio's Programmable Video JS SDK](https://github.com/twilio/twilio-video.js), [Twilio's Conversations JS SDK](https://www.npmjs.com/package/@twilio/conversations), and [Create React App](https://github.com/facebook/create-react-app).

The authorise method generates [an access token](https://www.twilio.com/docs/conversations/create-tokens) (in [JWT format](https://jwt.io/)) that is used [to connect to a room](https://github.com/twilio/twilio-video.js#usage). A step-by-step guide how [to join to a room could be found here](https://www.twilio.com/docs/video/javascript-getting-started#connect-to-a-room).
