---
description: Gets the search strings, keywords, and other information about an asset. The response contains additional information about the asset.
solution: Experience Manager
title: getSearchStrings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e94215b8-1121-4be6-a8a9-e9444c57495d
---
# getSearchStrings{#getsearchstrings}

Gets the search strings, keywords, and other information about an asset. The response contains additional information about the asset.

 Syntax 

## Authorized User Types {#section-b09c817a59f949a28e1c029e431f5698}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-c1efda4bb15349a68b276bafee8c18fd}

**Input (getSearchStringsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | Handle to the company.  |
|  assetHandle  | `xsd:string`  | Yes  | Handle to the asset.  |

**Output (getSearchStringsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  searchStringArray  | `types:SearchStrings`  | Yes  | An array of asset search strings.  |

## Examples {#section-e1f73bff6e4440c489d59cb9aa5384d8}

This code sample returns asset specific search strings. The response returns an empty array.

**Request** 

```java
<getSearchStringsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>47</ns1:companyHandle>
   <assetHandle>a|717|1|530</assetHandle>
</getSearchStringsParam>
```

**Response**

None.
