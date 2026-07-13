---
description: Gets all viewer configuration settings associated with the specified asset.
solution: Experience Manager
title: getViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: c0438238-8aab-4478-926a-fc0e11732fc1
TQID: 'https://experienceleague.adobe.com/GeSAS1EP7Q6EgsQltyC-TVnxS0zusuKxKs6QL8wfLWw'
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
|  companyHandle  | `xsd:string`  | Yes  | Handle to the company.  |
|  assetHandle  | `xsd:string`  | Yes  | Handle to the asset.  |

**Output (getViewerCoinfigSettingsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  type  | `xsd:string`  | Yes  | Viewer type to which the configuration settings apply.  |
|  configSettingsArray  | `types:ConfigSettingsArray`  | Yes  | Array of viewer configuration settings.  |

