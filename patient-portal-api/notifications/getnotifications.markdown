---
layout: page
title: GetNotifications
nav_order: 1
parent: Notifications
---

# GetNotifications

Returns notifications about appointments, invoices, questionnaires etc.

## JavaScript library method

```javascript
patientportal.notification.getNotifications({type: <type>});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/notification/notifications` |

## URL Parameters

<table>
    <thead>
        <tr>
            <th style="text-align: left">Parameter</th>
            <th style="text-align: left">Type</th>
            <th style="text-align: left">Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>type</td>
            <td>int (optional)</td>
            <td>
                <p>The type of the notification the client requests:</p>
                <ul>
                    <li>1 = Appointments that coming up soon</li>
                    <li>2 = Outstanding questionnaires</li>
                    <li>4 = Outstanding invoices</li>
                    <li>8 = Outstanding messages</li>
                    <li>16 = Action required</li>
                    <li>32 = Referral notification</li>
                    <li>64 = Membership payment required</li>
                </ul>
                <p>Note: The client can use a combination (sum) of several types. For example 1+4=5 returns
                    notifications about appointments that coming up soon and outstanding invoices.</p>
                <p>Default value is 95 (all but referral notifications)</p>
            </td>
        </tr>
    </tbody>
</table>

## Returns

[NotificationData](../objects-and-data-types/notificationdata)[]
