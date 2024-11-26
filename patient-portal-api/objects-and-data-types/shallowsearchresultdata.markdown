---
layout: page
title: ShallowSearchResultData
nav_order: 82
parent: Objects and data types
---

# ShallowSearchResultData

A shallow search result of a patient/company address.

## Properties

| Parameter | Type   | Description                                                 |
|:----------|:-------|:------------------------------------------------------------|
| Key | string | An encrypted key value containing partial address information used to retrieve complete address details. |
| Address | string | A single-line search result address. |

## JSON Example

```
{

"Key": "fc560b40315dc7605fd5ca53e0dcaabc357c69bea3faefa8c6e2ce8129909061956910b77338ee2c2cdbb1c7c5f7c64bcf338d78bc148f81f6786152d3ef2987b3ab5b1e5588b1db7939bb5e0edffec4614c4511c4a7a0dfd9bc9077749482b152217c572b0f78552c75be542ffcea6446110af6da78213c1f71569f35abab7d65f82f382f8b8dc663c8e6a1405bf17c331d379f375ffbc6ec3ebc21a985a69355d10622db48eceb7f23b38c5037ed2315c3d858268baae1879f6f84b3b65586742086832ec398acdfd56680a72991d7bb38bbfd1fa61991aebf0bd1982dc06b",

"Address": " 2 Paradise Street, Liverpool, Merseyside, L1 8JF"

}
```

###
