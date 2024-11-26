---
layout: page
title: Insurers
nav_order: 1
parent: Companies
---

# Insurers

Returns a list of insurers available for the current chamber. Only insurers marked as ‘public’ are returned.

## JavaScript library method

```javascript
PatientPortalCompanies.prototype.getInsurers();
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/companies/insurers` |

## Returns

[CompanyData\[\]](#_CompanyData)
