---
layout: page
title: CaseData
nav_order: 15
parent: Objects and data types
---

# CaseData

A full case data object which includes full patient demographic data.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Key | string | The unencrypted case key. |
| Patient | [PatientDemographicData](../objects-and-data-types/persondemographicdata) | The patient’s demographic details. |
| OpenedDate | [DateTime](../objects-and-data-types/datetime) | The date the case was opened. |
| ClosedDate | [DateTime](../objects-and-data-types/datetime) (optional) | The date the case was closed, if at all. |
| Title | string | The public case title. |
| IsOpen | bool | Whether the case is still open or not. |
