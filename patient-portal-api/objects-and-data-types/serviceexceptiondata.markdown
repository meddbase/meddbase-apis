---
layout: page
title: ServiceExceptionData
nav_order: 80
parent: Objects and data types
---

# ServiceExceptionDataProvides information about the exception.## Properties<table><tbody><tr><th><p>Message</p></th><th><p>string</p></th><th><p>Message of the exception.</p></th></tr><tr><td><p>EventType</p></td><td><p>int</p></td><td><p>Type of the exception:</p><ul><li>1 = Critical</li><li>2 = Error</li><li>4 = Warning</li><li>8 = Information</li></ul></td></tr><tr><td><p>EventCode</p></td><td><p>int</p></td><td><p>Specific code to identify the exception (argument missing, not logged in, not all required questions of the questionnaire are answered, etc.).</p></td></tr><tr><td><p>HttpStatusCode</p></td><td><p>int</p></td><td><p>Same like HTTP status code. See Error handling</p></td></tr><tr><td><p>Description</p></td><td><p>string</p></td><td><p>More details of the exception.</p></td></tr><tr><td><p>ReferenceNumber</p></td><td><p>string</p></td><td><p>A unique reference number that represents an event in the Meddbase logs. This can be traced by Meddbase support.</p></td></tr></tbody></table>## JSON Example```{"Message": "Password isn't set.","EventType": 2,"EventCode": 0,"HttpStatusCode": 400,"Description": null,"ReferenceNumber": null}```