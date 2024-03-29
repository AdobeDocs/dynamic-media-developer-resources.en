---
description: Updates SWF viewer configuration settings.
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 04565e2b-bda3-4ad0-afc1-2df01e455490
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
|  companyHandle  | `xsd:string`  | Yes  | Handle to the company.  |
|  assetHandle  | `xsd:string`  | Yes  | Asset handle.  |
|  configSettingArray  | `types:ConfigSettingArray`  | Yes  | Array of configuration settings you want to apply to the viewer.  |

**Output (updateViewerConfigSettingsReturn)**

The IPS API does not return a response for this operation.
