---
description: Attaches viewer configuration settings to an asset. These can be a viewer preset or the source asset for the viewer.
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 6b70f2c3-c98b-455f-b453-bb797744dadc
TQID: https://experienceleague.adobe.com/tDSXSL0VjiQbtC8IurBrnrAY5LEjQFkN6HyOmkFjiOU
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
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
|  companyHandle  | `xsd:string`  | Yes  | Handle to the company.  |
|  assetHandle  | `xsd:string`  | Yes  | Asset handle.  |
|  name  | `xsd:string`  | Yes  | Asset name.  |
|  type  | `xsd:string`  | Yes  | The type of asset you want to apply the viewer configuration to.  |
|  configSettingArray  | `types:ConfigSettingArray`  | Yes  |The array of `ConfigSettings` applied to the asset..  |

**Output (setViewerConfigSettingsParam)**

The IPS API does not return a response for this operation.
