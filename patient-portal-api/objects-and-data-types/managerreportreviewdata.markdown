---
layout: page
title: ManagerReportReviewData
nav_order: 45
parent: Objects and data types
---

# ManagerReportReviewData

Provides information about the manager review.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| ReportUrl | string | The URL address of the full medical report. The report is PDF document.<br><br>We recommend to use &lt;object&gt; tag to display embedded PDF:<br><br>&lt;object type="application/pdf" data="<url&gt;">&lt;/object&gt; |
| ReferredBy | string | The name of the referrer. |
| Referral | ReferralData | The referral data. |

## JSON Example

```json
{
    "ReportUrl": "http://api.meddbase.com/patientportalapi/...",
    "ReferredBy": "Mr. John Smith",
    "Referral": {
        "Key": "R123",
        "PatientName": "Mr. John Smith",
        "ReferredBy": "Mr. Will Smith",
        "CreatedDate": "2015-03-13T14:22:12",
        "ModifiedDate": "2015-03-13T14:52:30",
        "State": "InProgress",
        "StateDisplayName": "In progress",
        "StateColor": "green",
        "ReferralNumber": 13911,
        "AppointmentType": {
            "Name": "Referral",
            "Key": "REF1",
            "Notes": "",
            "CanBookAppointment": true,
            "CanReferPatient": true
        },
        "Appointments": [
            {
                "Key": "apt58462",
                "Type": {
                    "Key": "CN",
                    "Name": "Consultation"
                },
                "Start": "2013-08-07T09:30:00",
                "Finish": "2013-08-07T10:30:00",
                "Telemedicine": true,
                "TelemedicineConnection": "http://Meddbase.sandboxga.com/flex.html?roomdirect.html&key=Wchof474qrCO2QLrNK1SEMdrRY",
                "AuthorisationCode": "ABC123",
                "Site": {
                    "Key": 1123,
                    "Name": "2CP (Eye Room)",
                    "Address": {
                        "Address1": "2 Clifton Park Ave",
                        "Address2": "",
                        "Address3": "",
                        "City": "London",
                        "County": "",
                        "PostCode": "SW20 8BD",
                        "Country": "United Kingdom"
                    }
                },
                "Location": {
                    "Key": 214,
                    "Name": "Room 1",
                    "Address": {
                        "Address1": "2 Clifton Park Ave",
                        "Address2": "",
                        "Address3": "",
                        "City": "London",
                        "County": "",
                        "PostCode": "SW20 8BD",
                        "Country": "United Kingdom"
                    }
                },
                "Clinician": {
                    "Key": 84,
                    "Name": "Dr. House"
                },
                "Slots": [
                    {
                        "Type": "CN",
                        "Start": "2013-08-07T09:30:00",
                        "Finish": "2013-08-07T10:30:00",
                        "SiteKey": 1123,
                        "LocationKey": 214,
                        "ResourceKey": 468
                    }
                ],
                "PrimaryAttendeeSlot": {
                    "Type": "CN",
                    "Start": "2013-08-07T09:30:00",
                    "Finish": "2013-08-07T10:30:00",
                    "SiteKey": 1123,
                    "LocationKey": 214,
                    "ResourceKey": 468
                },
                "Invoice": {
                    "Key": "inv4645",
                    "Date": "2013-02-06",
                    "Number": "1865",
                    "CurrencyCode": "GBP",
                    "CurrencySymbol": "£",
                    "TotalNet": 200,
                    "Tax": 40,
                    "TotalGross": 240,
                    "Paid": 150,
                    "Creditor": {
                        "Name": "AXA PPP Healthcare",
                        "IsCompany": true,
                        "Address": {
                            "Address1": "44 Pall Mall",
                            "City": "London",
                            "PostCode": "SW1Y",
                            "Country": "United Kingdom"
                        },
                        "Account": {
                            "CODE": "AXA",
                            "Name": "AXA PPP Healthcare",
                            "Address": {
                                "Address1": "44 Pall Mall",
                                "City": "London",
                                "PostCode": "SW1Y",
                                "Country": "United Kingdom"
                            }
                        }
                    },
                    "Debtor": {
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
                        "Account": {
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
                    },
                    "PayableOnline": true
                }
            }
        ],
        "Questionnaires": [
            {
                "Key": "q123",
                "Name": "Referral",
                "Description": "",
                "StatusCode": 1,
                "Status": "1",
                "Expiration": "2015-03-26T14:37:00.2003719+00:00"
            }
        ],
        "Documents": [
            {
                "Name": "Referral letter.html",
                "Author": "Mr. Will Smith",
                "Comment": "I would like to refer Mr. John Smith",
                "DateCreated": "2015-03-13T14:22:12.483",
                "Url": "https://api.meddbase.com/referrals/download?d=123",
                "MIMEType": "text/html",
                "Size": 20824
            }
        ],
        "CanCancel": false,
        "CanBookAppointment": false,
        "CanSend": false,
        "CanReallocate": true,
        "CanCollaborate": true,
        "CanAttachDocument": false,
        "CanFollowUp": false,
        "PatientReview": {
            "Required": true,
            "InProgress": false,
            "Finished": false,
            "State": "Not started"
        },
        "AbsenceRecordKey": "123",
        "RejectionReason": "Holidays",
        "PublicReasonForReferral": "Angina",
        "DaysToReviewDischargeLetterByPatient": 3
    }
}
```
