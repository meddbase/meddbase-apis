---
layout: page
title: FuzzySearch
nav_order: 2
parent: Address Finder
---

# FuzzySearch

Returns a number of possible shallow search address results for the search term query.

## JavaScript library method

```javascript
patientportal.addressFinder.fuzzySearch({query: <query>});
```

## HTTP Method

GET

## ****Url****

/patientportalapi/address-finder/fuzzy-search

## URL Parameters

| query | string | Case-insensitive search term query relating to a desired address. |
| --- | --- | --- |

## Returned JSON

```
[Shallow Search Result Data](#_ShallowSearchResultData)\[\]
```
