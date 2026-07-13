---
description: Updates SWF viewer configuration settings.
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 04565e2b-bda3-4ad0-afc1-2df01e455490
TQID: 'https://experienceleague.adobe.com/YcfK5U6MKvmV2ulOQ3s2sOOBsgASSeslCIrk87xLAv8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
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

