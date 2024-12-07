---
layout: page
title: NotificationData
nav_order: 49
parent: Objects and data types
---

# NotificationData

Provides information about notification (outstanding invoice or questionnaire, etc.).

## Properties

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
            <td>Key</td>
            <td>string</td>
            <td>Key of the notification.</td>
        </tr>
        <tr>
            <td>Type</td>
            <td>int</td>
            <td>
                <p>The type of the notification:</p>
                <ul>
                    <li>1 = Appointment coming up soon</li>
                    <li>2 = Outstanding questionnaire</li>
                    <li>4 = Outstanding invoice</li>
                    <li>8 = Outstanding messages</li>
                    <li>16 = Action required</li>
                    <li>32 = Referral notification</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Message</td>
            <td>string</td>
            <td>Message of the notification.</td>
        </tr>
        <tr>
            <td>ObjectKey</td>
            <td>string</td>
            <td>
                <p>Key of the related object to this notification according to the Type of the notification (e.g.
                    notification of type 2 ‘Outstanding questionnaire’ relates to the questionnaire so the object key
                    means the questionnaire key).</p>
                <p>By the Type the ObjectKey means:</p>
                <ul>
                    <li>1 = appointment key</li>
                    <li>2 = questionnaire key</li>
                    <li>4 = invoice key</li>
                    <li>8 = feed key</li>
                    <li>16 =<ul>
                            <li>‘SetContactOptions’ to force patient to set their contact options.</li>
                            <li>‘AcceptTermsAndConditions’ to force patient to re-accept the Terms and conditions.</li>
                        </ul>
                    </li>
                    <li>32 = referral key</li>
                </ul>
                <p>The client can use this key to redirect/show more details about related objects.</p>
            </td>
        </tr>
    </tbody>
</table>

## JSON Example

```json
{
    "Key": "2-1568",
    "Type": 1,
    "Message": "You need to complete pre-medical questionnaire.",
    "ObjectKey": "1568"
}
```
