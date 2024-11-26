---
layout: page
title: PersonDemographicData
nav_order: 64
parent: Objects and data types
---

# PersonDemographicData

Contains the person’s demographic information (e.g. patient’s demographic data).

## Properties

<table><tbody><tr><th><p>Key</p></th><th><p>string</p></th><th><p>Key of the person.</p></th></tr><tr><td><p>Title</p></td><td><p>string</p></td><td></td></tr><tr><td><p>Name</p></td><td><p>string</p></td><td></td></tr><tr><td><p>Surname</p></td><td><p>string</p></td><td></td></tr><tr><td><p>SexType</p></td><td><p>int</p></td><td><p>Biological sex at birth:</p><ul><li>0 = any</li><li>1 = male</li><li>2 = female</li></ul></td></tr><tr><td><p>Gender</p></td><td><p>GenderData</p></td><td><p>The person’s gender identity.</p></td></tr><tr><td><p>Pronoun</p></td><td><p>PronounData</p></td><td><p>The person’s preferred pronouns.</p></td></tr><tr><td><p>Initials</p></td><td><p>string</p></td><td></td></tr><tr><td><p>DateOfBirth</p></td><td><p>DateTime</p></td><td></td></tr><tr><td><p>Mobile</p></td><td><p>string</p></td><td></td></tr><tr><td><p>Telephone</p></td><td><p>string</p></td><td></td></tr><tr><td><p>EmailAddress</p></td><td><p>string</p></td><td><p>Personal email address. This address is used to log into the patient portal.</p></td></tr><tr><td><p>WorkTelephone</p></td><td><p>string</p></td><td></td></tr><tr><td><p>WorkEmailAddress</p></td><td><p>string</p></td><td><p>Work email address. This address is used to log into the referral portal.</p></td></tr><tr><td><p>Password</p></td><td><p>string</p></td><td><p>Used only for registration. Should be at least 8 characters long and should contain at least 1 numbers, 1 capital letter and 1 small letter. API never returns the password. It is for submitting only.</p></td></tr><tr><td><p>Address</p></td><td><p>AddressData</p></td><td></td></tr><tr><td><p>NextOfKin</p></td><td><p>NextOfKinDemographicData</p></td><td></td></tr><tr><td><p>ContactOptions</p></td><td><p>PatientContactOption[]</p></td><td></td></tr><tr><td><p>TermsAndConditionsAccepted</p></td><td><p>bool</p></td><td></td></tr><tr><td><p>StatisticalProcessingAccepted</p></td><td><p>bool</p></td><td></td></tr><tr><td><p>EmployeeNumber</p></td><td><p>string</p></td><td><p>The employee number.</p></td></tr><tr><td><p>EmployeeDepartment</p></td><td><p>DepartmentData</p></td><td><p>The department the employee belongs to. Could be null.</p></td></tr><tr><td><p>EmployeeDivision</p></td><td><p>DivisionData</p></td><td><p>The division the employee belongs to. Could be null.</p></td></tr><tr><td><p>EmployeeStatus</p></td><td><p>EmployeeStatus</p></td><td><p>The status of the employee.</p></td></tr><tr><td><p>Permissions</p></td><td><p>object</p><p>See GetConfig for details.</p></td><td><p>The permissions of the logged-in user for this person. This could be different to the permissions provided upon GetConfig.</p></td></tr><tr><td><p>Insurer</p></td><td><p><a href="#_InsurerData">InsurerData</a></p></td><td><p>Insurer Data for the patient. Only available for patient portal. When setting patient demographics, only public company key’s can be used to set the Insurer.</p></td></tr><tr><td><p>EmployerName</p></td><td><p>String</p></td><td><p>The name of the employer.</p></td></tr><tr><td><p>EmployerAddress</p></td><td><p>AddressData</p></td><td><p>The employer address.</p></td></tr><tr><td><p>ReferrerKey</p></td><td><p>string</p></td><td><p>Encrypted key of the referrer. The set of valid values are obtained by call to <a href="#_Referrers">getReferrers</a>. Can be null.</p></td></tr><tr><td><p>EthnicityKey</p></td><td><p>string</p></td><td><p>Encrypted key of the person’s ethnicity. The set of valid values are obtained by call to <a href="#_Ethnicities">getEthnicities</a>. Can be null.</p></td></tr></tbody></table>

## JSON Example

```
{

"Title": "Mr",

"Name": "John",

"Surname": "Lemon",

"SexType": 1,

"Initials": "JL",

"DateOfBirth": "1958-08-02T00:00:00",

"Mobile": "+444 895 523 411",

"Telephone": "+444 525 111 555",

"EmailAddress": "<john.lemon@test.com>",

"WorkEmailAddress": "<john.lemon@mywork.com>",

"Password": "jon4535lemon",

"Address": {

"Address1": "Studio 99",

"Address2": "Backlok Street",

"Address3": "Camden",

"City": "London",

"County": "",

"PostCode": "N1 7NK",

"Country": "United Kingdom"

},

"NextOfKin": {

"Relationship": "Mam",

"Name": "Mariel",

"Surname": "Lemon",

"Mobile": "+444 895 111 222",

"WorkTelephone": "+444 525 111 555",

"Address": {

"Address1": "Studio 1",

"Address2": "Cardwell Roa",

"Address3": "Camden",

"City": "London",

"County": "",

"PostCode": "N1 7NK",

"Country": "United Kingdom"

}

}

}
```
