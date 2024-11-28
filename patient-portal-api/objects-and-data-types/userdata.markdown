---
layout: page
title: UserData
nav_order: 88
parent: Objects and data types
---

# UserData

Provides information about the user. The UserData object inherits the [PersonDemographicData](../objects-and-data-types/persondemographicdata).

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Key | string | The key of the user. This key doesn’t equal the key of the patient. |
| <PersonDemographicData properties> |     | The UserData object inherits the [PersonDemographicData](../objects-and-data-types/persondemographicdata). |
| Rights | [UserRights](../objects-and-data-types/userrights)[] | The list of user rights. |
| AllPatientsVisible | bool | If True then all patients within the company are visible and the list of accessible departments is ignored. |
| AllNonAssignedPatientsVisible | bool | If True then all patients who do not have a department set up within the company are visible. |
| AccessibleDepartments | [DepartmentData](../objects-and-data-types/departmentdata)[] | The list of departments the user has got an access to manage. |
| AllDocumentTypesVisible |     | If True then all document typse within the company are visible.<br><br>This applies if the DocumentTypeSecurityEnable flag is set (see GetConfig) |
| AccessibleDocumentTypes | [DocumentType](../objects-and-data-types/documenttype)[] | The list of document types the user has got an access to see.<br><br>This applies if the DocumentTypeSecurityEnable flag is set (see GetConfig) |
| LastLogin | DateTime | The last login date. Date could be null. |

## JSON Example

```json
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
    },
    "AllPatientsVisible": false,
    "AllNonAssignedPatientsVisible": false,
    "Rights": [
        {
            "Key": "0f0f8997-a161-455e-a498-96138096f539",
            "Name": "Case management",
            "Description": "The user can refer patients and manage the referrals."
        }
    ],
    "AccessibleDepartments": [
        {
            "Key": "D01",
            "Name": "HR"
        },
        {
            "Key": "D02",
            "Name": "Research"
        }
    ],
    "LastLogin": "2015-01-01T10:41:10.547"
}
```
