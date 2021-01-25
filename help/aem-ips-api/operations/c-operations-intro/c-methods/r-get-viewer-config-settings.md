---
description: Gets all viewer configuration settings associated with the specified asset.
seo-description: Gets all viewer configuration settings associated with the specified asset.
seo-title: getViewerConfigSettings
solution: Experience Manager
title: getViewerConfigSettings
topic: Dynamic Media Image Production System API
uuid: 61fe16de-ac72-472b-8945-f1ebe8b4d11c
---

# getViewerConfigSettings{#getviewerconfigsettings}

Gets all viewer configuration settings associated with the specified asset.

 Syntax 

## Authorized User Types {#section-05c3ea8f7d2d42c6bf7af63e03f457a9}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-7d06abf3d707494c8a1270c7fa1477f1}

**Input (getViewerConfigSettingsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | Handle to the company.  |
|  `*`assetHandle`*`  | `xsd:string`  | Yes  | Handle to the asset.  |

**Output (getViewerCoinfigSettingsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`type`*`  | `xsd:string`  | Yes  | Viewer type to which the configuration settings apply.  |
|  `*`configSettingsArray`*`  | `types:ConfigSettingsArray`  | Yes  | Array of viewer configuration settings.  |

