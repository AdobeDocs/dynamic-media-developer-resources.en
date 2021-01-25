---
description: Checks for IPS ID conflicts by comparing asset names against all names a company's Image Serving/Image Rendering catalog namespace.
seo-description: Checks for IPS ID conflicts by comparing asset names against all names a company's Image Serving/Image Rendering catalog namespace.
seo-title: checkAssetNames
solution: Experience Manager
title: checkAssetNames
topic: Dynamic Media Image Production System API
uuid: 91d073a8-7648-429b-aa5c-c7d595550299
---

# checkAssetNames{#checkassetnames}

Checks for IPS ID conflicts by comparing asset names against all names a company's Image Serving/Image Rendering catalog namespace.

 Syntax 

## Authorized User Types {#section-8efcbb3f555f417a870219e4714374db}

* `IpsUser` 
* `IpsAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser` 
* `ImagePortalUser` 
* `TrialSiteAdmin` 
* `TrialSiteUser`

## Parmaeters {#section-9c75b00f2072453abea0bdefc6ad7c99}

**Input (checkAssetNamesParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | No  | The handle to the company that contains the user.  |
|  `*`assetNamesArray`*`  | `types:StringArray`  | Yes  | An array of asset names to check.  |

**Output (checkAssetNamesReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`inUseNameArray`*`  | `types:StringArray`  | Yes  | An array of asset names in use.  |

## Examples {#section-bc5d120d74614a63a425ca3acc337219}

This sample code requests the asset names in use for a specified company. The response returns an array of asset names that are in use.

**Request** 

```java
<checkAssetNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <companyHandle>c|1</companyHandle>
   <assetNameArray>
      <items>ABC123</items>
      <items>DEF456</items>
   </assetNameArray>
</checkAssetNamesParam>
```

**Response** 

```java
<checkAssetNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <inUseNameArray>
      <items>DEF456</items>
   </inUseNameArray>
</checkAssetNamesReturn>
```

