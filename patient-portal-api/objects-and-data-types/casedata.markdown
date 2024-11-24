---
layout: page
title: CaseData
nav_order: 15
parent: Objects and data types
---

# CaseDataA full case data object which includes full patient demographic data.## Properties| Key | string | The unencrypted case key. || --- | --- | --- || Patient | [PatientDemographicData](#_PersonDemographicData) | The patient’s demographic details. || OpenedDate | [DateTime](#_DateTime) | The date the case was opened. || ClosedDate | [DateTime](#_DateTime) (optional) | The date the case was closed, if at all. || Title | string | The public case title. || IsOpen | bool | Whether the case is still open or not. |