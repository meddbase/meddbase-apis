---
layout: page
title: AuthenticationData
nav_order: 13
parent: Objects and data types
---

# AuthenticationData

Contains the information about current authenticated security context.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| SessionID | string | Identifies the existing security context. |
| Config | ConfigData | Defines that the patient should be forced to set up their contact options. |
| Token | string | The current token. See Authentication Token. |
| Require2FA | Boolean | True if the profile requires 2FA (see Send2faCode). False if the profile does not require 2FA. |

## JSON Example

```json
{
    "SessionID": "4oytawakgy0njpaajyliq3md",
    "Config": {
        "IsLoggedIn": true,
        "CompanyName": "Test Company",
        "Phone": "077123456789",
        "Permissions": {
            "Patient": {
                "CanBookAppointment": false,
                "CanViewAppointments": false,
                "CanCancelAppointment": false,
                "CanViewInvoices": false,
                "CanPayInvoice": false,
                "CanViewMedicalHistory": false,
                "CanManageQuestionnaires": false,
                "CanManageFeeds": false,
                "CanViewCompanyLibrary": false,
                "CanViewPathways": false,
                "CanChangePassword": false
            },
            "User": {
                "CanManageUsers": true,
                "CanViewReferrals": true,
                "CanViewReferralReports": true,
                "CanReferPatient": true,
                "CanBulkReallocateReferrals": true,
                "CanViewRecall": true,
                "CanViewDocument": true,
                "CanViewAppointment": true,
                "CanChangePassword": true,
                "CanViewPathways": true
            }
        },    
        "Configuration": {
            "OnlinePaymentsEnabled": true,
            "DateOfBirthRequiredForPatients": true,
            "SSOStatus": {
                "Identifier": "shiny",
                "Enabled": true,
                "IsOH": true
            },
            "PasswordPolicy": {
                "Length": 10,
                "Numbers": 1,
                "Letters": 1,
                "NonAlphaNumeric": 0,
                "MixCaps": true,
                "Description": "at least 10 characters in length, contain at least one letter an done number and must mix upper and lower-case letters"
            },
            "DefaultCallingCode": "+44",
            "NhsConsentEnabled": false,
            "SessionTimeout": 120000,
            "DefaultPaymentCountry": "GB"
        },
        "ForceContactOptions": false,
        "ForceTermsAndConditions": false
    },
    "Token": "7a413802-f186-42c6-ae92-646531749624",
    "Require2FA": "true"
}
```
