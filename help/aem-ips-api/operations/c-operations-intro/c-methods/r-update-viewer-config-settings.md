---
description: Updates SWF viewer configuration settings.
seo-description: Updates SWF viewer configuration settings.
seo-title: updateViewerConfigSettings
solution: Experience Manager
title: updateViewerConfigSettings
topic: Scene7 Image Production System API
uuid: ad4af874-5ca4-4182-868e-afa48b1cd2b6
index: y
internal: n
snippet: y
---

# updateViewerConfigSettings{#updateviewerconfigsettings}

Updates SWF viewer configuration settings.

 Syntax 

## Authorized User Types {#section-0dd001da1b784aefa5eb5b50c7a2c045}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-29790d933fb24aa392d0cb2d52d1310f}

**Input (updateViewerConfigSettingsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`companyHandle`*`  | `xsd:string`  | Yes  | Handle to the company.  |
|  ` *`assetHandle`*`  | `xsd:string`  | Yes  | Asset handle.  |
|  ` *`configSettingArray`*`  | `types:ConfigSettingArray`  | Yes  | Array of configuration settings you want to apply to the viewer.  |

**Output (updateViewerConfigSettingsReturn)**

The IPS API does not return a response for this operation. 
