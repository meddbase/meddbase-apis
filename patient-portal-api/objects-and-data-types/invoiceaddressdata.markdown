---
layout: page
title: InvoiceAddressData
nav_order: 38
parent: Objects and data types
---

# InvoiceAddressData

Contains information about the invoice’s creditor or debtor.

## Properties

| Name | string | Name of the account. |
| --- | --- | --- |
| IsCompany | bool | True if the account is a company. False if the account is a patient. |
| Address | AddressData | Account address. |
| Account | CompanyDemographicData<br><br>PersonDemographicData | A demographic data of the account.<br><br>If the IsCompany is true, the type of this property is CompanyDemographicData, else the type is PersonDemographicData. |

## JSON Example

```
{

"Name": "Mr. John Lemon",

"IsCompany": false,

"Address": {

"Address1": "Studio 99",

"Address2": "Backlok Street",

"Address3": "Camden",

"City": "London",

"County": "",

"PostCode": "N1 7NK",

"Country": "United Kingdom"

},

Account: {

"Title": "Mr",

"Name": "John",

"Surname": "Lemon",

"SexType": 1,

"Initials": "JL",

"DateOfBirth": "1958-08-02T00:00:00",

"Mobile": "+444 895 523 411",

"Telephone": "+444 525 111 555",

"EmailAddress": "<john.lemon@test.com>",

"Address": {

"Address1": "Studio 99",

"Address2": "Backlok Street",

"Address3": "Camden",

"City": "London",

"County": "",

"PostCode": "N1 7NK",

"Country": "United Kingdom"

}

}

}
```
