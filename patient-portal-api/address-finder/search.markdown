---
layout: page
title: Search
nav_order: 1
parent: Address Finder
---

# Search

Returns a number of possible shallow search address results for the postcode.

## JavaScript library method

```javascript
patientportal.addressFinder.search({postcode: <postcode>});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/address-finder/search` |

## URL Parameters

| postcode | string | Case-insensitive postcode with space (e.g. N7 0NH or n7 0nh). |
| --- | --- | --- |

## Returned JSON

```
[Shallow Search Result Data](#_ShallowSearchResultData)\[\]
```

Returns a number of possible shallow search address results for the postcode.

## JavaScript library method

```javascript
patientportal.addressFinder.search({postcode: <postcode>});
```

## HTTP Method

| Verb | URL                                               |
|:-----|:--------------------------------------------------|
| GET | `/patientportalapi/address-finder/search` |

## URL Parameters

| postcode | string | Case-insensitive postcode with space (e.g. N7 0NH or n7 0nh). |
| --- | --- | --- |

## Returned JSON

Shallow Search Result Data\[\]
