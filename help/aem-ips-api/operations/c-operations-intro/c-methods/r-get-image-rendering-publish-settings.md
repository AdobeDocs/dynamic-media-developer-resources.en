---
description: For internal use only. See the Image Rendering Material Catalog Reference–Catalog Attributes section.
solution: Experience Manager
title: getImageRenderingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 152dfd61-2fba-47b4-8e69-fbbc8fb57f87
TQID: https://experienceleague.adobe.com/GNxFN5oGHkMpwmV3jLFe-vtEHrnxFlTxzvf4idwc7gw
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

For internal use only. See the Image Rendering Material Catalog Reference–Catalog Attributes section.

Syntax 

## Authorized User Types {#section-1097e0563c61480a8e97822dc3527070}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-4f2cb8c589384816bb2525654ec49963}

**Input (getImageRenderingPublishSettingsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | The handle to the company whose image rendering publishing settings you wish to get.  |
|  contextHandle  | `xsd:string`  | Yes  | Handle to the publish context.  |

**Output (getImageRenderingPublishSettingsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  publishSettingsArray  | `type:ConfigSettingArray`  | Yes  | Image rendering publishing settings.  |
