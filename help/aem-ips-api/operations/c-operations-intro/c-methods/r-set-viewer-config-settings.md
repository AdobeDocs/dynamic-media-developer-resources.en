---
description: Attaches viewer configuration settings to an asset. These can be a viewer preset or the source asset for the viewer.
seo-description: Attaches viewer configuration settings to an asset. These can be a viewer preset or the source asset for the viewer.
seo-title: setViewerConfigSettings
solution: Experience Manager
title: setViewerConfigSettings
topic: Scene7 Image Production System API
uuid: d83d866e-9243-479f-9b33-727aad8158e5
---

# setViewerConfigSettings{#setviewerconfigsettings}

Attaches viewer configuration settings to an asset. These can be a viewer preset or the source asset for the viewer.

 Syntax 

## Authorized User Types {#section-81c429ba9f4c4359986a30ea7ebea8d2}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-bcc8c83cc84141e8b1341be9133e8511}

**Input (setViewerConfigSettingsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`companyHandle`*`  | `xsd:string`  | Yes  | Handle to the company.  |
|  ` *`assetHandle`*`  | `xsd:string`  | Yes  | Asset handle.  |
|  ` *`name`*`  | `xsd:string`  | Yes  | Asset name.  |
|  ` *`type`*`  | `xsd:string`  | Yes  | The type of asset you want to apply the viewer configuration to.  |
|  ` *`configSettingArray`*`  | `types:ConfigSettingArray`  | Yes  |The array of `ConfigSettings` applied to the asset..  |

**Output (setViewerConfigSettingsParam)**

The IPS API does not return a response for this operation. 
