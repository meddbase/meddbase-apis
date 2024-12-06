---
layout: page
title: PersonDemographicData
nav_order: 64
parent: Objects and data types
---

# PersonDemographicData

Contains the person’s demographic information (e.g. patient’s demographic data).

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
            <td>Key of the person.</td>
        </tr>
        <tr>
            <td>Title</td>
            <td>string</td>
            <td></td>
        </tr>
        <tr>
            <td>Name</td>
            <td>string</td>
            <td></td>
        </tr>
        <tr>
            <td>Surname</td>
            <td>string</td>
            <td></td>
        </tr>
        <tr>
            <td>SexType</td>
            <td>int</td>
            <td>
                <p>Biological sex at birth:</p>
                <ul>
                    <li>0 = any</li>
                    <li>1 = male</li>
                    <li>2 = female</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Gender</td>
            <td><a href="../objects-and-data-types/genderdata">GenderData</a></td>
            <td>The person’s gender identity.</td>
        </tr>
        <tr>
            <td>Pronoun</td>
            <td><a href="../objects-and-data-types/pronoundata">PronounData</a></td>
            <td>The person’s preferred pronouns.</td>
        </tr>
        <tr>
            <td>Initials</td>
            <td>string</td>
            <td></td>
        </tr>
        <tr>
            <td>DateOfBirth</td>
            <td><a href="../objects-and-data-types/datetime">DateTime</a></td>
            <td></td>
        </tr>
        <tr>
            <td>Mobile</td>
            <td>string</td>
            <td></td>
        </tr>
        <tr>
            <td>Telephone</td>
            <td>string</td>
            <td></td>
        </tr>
        <tr>
            <td>EmailAddress</td>
            <td>string</td>
            <td>Personal email address. This address is used to log into the patient portal.</td>
        </tr>
        <tr>
            <td>WorkTelephone</td>
            <td>string</td>
            <td></td>
        </tr>
        <tr>
            <td>WorkEmailAddress</td>
            <td>string</td>
            <td>Work email address. This address is used to log into the referral portal.</td>
        </tr>
        <tr>
            <td>Password</td>
            <td>string</td>
            <td>
                <p>Used only for registration. Should be at least 8 characters long and should contain at least 1
                    numbers, 1 capital letter and 1 small letter. API never returns the password. It is for submitting
                    only.</p>
            </td>
        </tr>
        <tr>
            <td>Address</td>
            <td><a href="../objects-and-data-types/addressdata">AddressData</a></td>
            <td></td>
        </tr>
        <tr>
            <td>NextOfKin</td>
            <td><a href="../objects-and-data-types/nextofkindemographicdata">NextOfKinDemographicData</a></td>
            <td></td>
        </tr>
        <tr>
            <td>ContactOptions</td>
            <td><a href="../objects-and-data-types/patientcontactoption">PatientContactOption</a>[]</td>
            <td></td>
        </tr>
        <tr>
            <td>TermsAndConditionsAccepted</td>
            <td>bool</td>
            <td></td>
        </tr>
        <tr>
            <td>StatisticalProcessingAccepted</td>
            <td>bool</td>
            <td></td>
        </tr>
        <tr>
            <td>EmployeeNumber</td>
            <td>string</td>
            <td>The employee number.</td>
        </tr>
        <tr>
            <td>EmployeeDepartment</td>
            <td><a href="../objects-and-data-types/departmentdata">DepartmentData</a></td>
            <td>The department the employee belongs to. Could be null.</td>
        </tr>
        <tr>
            <td>EmployeeDivision</td>
            <td><a href="../objects-and-data-types/divisiondata">DivisionData</a></td>
            <td>The division the employee belongs to. Could be null.</td>
        </tr>
        <tr>
            <td>EmployeeStatus</td>
            <td><a href="../objects-and-data-types/employeestatus">EmployeeStatus</a></td>
            <td>The status of the employee.</td>
        </tr>
        <tr>
            <td>Permissions</td>
            <td>
                <p>object</p>
                <p>See GetConfig for details.</p>
            </td>
            <td>
                <p>The permissions of the logged-in user for this person. This could be different to the permissions
                    provided upon GetConfig.</p>
            </td>
        </tr>
        <tr>
            <td>Insurer</td>
            <td><a href="../objects-and-data-types/insurerdata">InsurerData</a></td>
            <td>
                <p>Insurer Data for the patient. Only available for patient portal. When setting patient demographics,
                    only public company key’s can be used to set the Insurer.</p>
            </td>
        </tr>
        <tr>
            <td>EmployerName</td>
            <td>string</td>
            <td>The name of the employer.</td>
        </tr>
        <tr>
            <td>EmployerAddress</td>
            <td><a href="../objects-and-data-types/addressdata">AddressData</a></td>
            <td>The employer address.</td>
        </tr>
        <tr>
            <td>ReferrerKey</td>
            <td>string</td>
            <td>
                <p>Encrypted key of the referrer. The set of valid values are obtained by call to <a
                        href="#_Referrers">getReferrers</a>. Can be null.</p>
            </td>
        </tr>
        <tr>
            <td>EthnicityKey</td>
            <td>string</td>
            <td>
                <p>Encrypted key of the person’s ethnicity. The set of valid values are obtained by call to <a
                        href="#_Ethnicities">getEthnicities</a>. Can be null.</p>
            </td>
        </tr>
    </tbody>
</table>

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
    }
}
```
