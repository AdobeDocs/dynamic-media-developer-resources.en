---
description: Returns the publish history for an asset.
solution: Experience Manager
title: getAssetPublishHistory
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f337e7f9-1af6-4164-b9bd-e697548e2850
---
# getAssetPublishHistory{#getassetpublishhistory}

Returns the publish history for an asset.

 Syntax 

## Authorized User Types {#section-3b9d6a129093458fa8890139a2718912}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-3541bd9914a44b89acfc1d419b560ee6}

**Input (getAssetPublishHistoryParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | The handle to the company with the asset publish history.  |
|  assetHandle  | `xsd:string`  | Yes  | The asset with the publish history you want to examine.  |

**Output (getAssetPublishHistoryReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  pubHistoryArray  | `types:PublishHistoryArray`  | Yes  | The asset's publish history.  |

## Examples {#section-53897c51e5a047c5bd5ea5a6efb2d114}

This code sample returns the publish history of an asset. An asset has never been published if the server returns an empty array.

**Request** 

```java
<getAssetPublishHistoryParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|732|1|535</assetHandle>
</getAssetPublishHistoryParam>
```

**Response** 

```java
<getAssetPublishHistoryReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <pubHistoryArray/>
</getAssetPublishHistoryReturn>
```
