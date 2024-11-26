---
layout: page
title: CaseOverviewData
nav_order: 16
parent: Objects and data types
---

# CaseOverviewData

A full case data object which includes the patient’s full name.

## Properties

| Key | string | The unencrypted case key. |
| --- | --- | --- |
| PatientName | string | The name of the patient. |
| OpenedDate | [DateTime](#_DateTime) | The date the case was opened. |
| ClosedDate | [DateTime](#_DateTime) (optional) | The date the case was closed, if at all. |
| LastUpdatedDate | [DateTime](#_DateTime) (optional) | The date that the latest change was made to any of the referrals on the case. If there are no referrals on the case, this date is null. |
| Title | string | The public case title. |
| IsOpen | bool | Whether the case is still open or not. |
