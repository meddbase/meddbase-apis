---
layout: page
title: UserData
nav_order: 88
parent: Objects and data types
---

# UserData

Provides information about the user. The UserData object inherits the PersonDemographicData.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Key | string | The key of the user. This key doesn’t equal the key of the patient. |
| &lt;PersonDemographicData properties&gt; |     | The UserData object inherits the PersonDemographicData. |
| Rights | User\[\] | The list of user rights. |
| AllPatientsVisible | bool | If True then all patients within the company are visible and the list of accessible departments is ignored. |
| AllNonAssignedPatientsVisible | bool | If True then all patients who do not have a department set up within the company are visible. |
| AccessibleDepartments | DepartmentData\[\] | The list of departments the user has got an access to manage. |
| AllDocumentTypesVisible |     | If True then all document typse within the company are visible.<br><br>This applies if the DocumentTypeSecurityEnable flag is set (see GetConfig) |
| AccessibleDocumentTypes | DocumentType\[\] | The list of document types the user has got an access to see.<br><br>This applies if the DocumentTypeSecurityEnable flag is set (see GetConfig) |
| LastLogin | DateTime | The last login date. Date could be null. |

## JSON Example

```
{

"&lt;PersonDemographicData properties &gt;": &lt;values&gt;,

"AllPatientsVisible": false,

"AllNonAssignedPatientsVisible": false,

"Rights": \[

{

"Key": "0f0f8997-a161-455e-a498-96138096f539",

"Name": "Case management",

"Description": "The user can refer patients and manage the referrals."

}

\],

"AccessibleDepartments": \[

{

"Key": "D01",

"Name": "HR"

},

{

"Key": "D02",

"Name": "Research"

}

\],

"LastLogin": "2015-01-01T10:41:10.547"

}
```
