---
description: For internal use only. Users should refer to the Image Serving Image Catalog Reference – Attribute Reference section.
solution: Experience Manager
title: getImageServingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ab7b5df6-58fb-4111-be9c-76901534d167
TQID: 'https://experienceleague.adobe.com/-VBxIs4EWFDesksSnU-DpN2pg-LJUN60OPhqjQVqAr8'
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
# getImageServingPublishSettings{#getimageservingpublishsettings}

For internal use only. Users should refer to the Image Serving Image Catalog Reference – Attribute Reference section.

 Syntax 

## Authorized User Types {#section-49b7b277ba1748499121a0e90996458c}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-79f0d54acd604ad2a5c96679334f2424}

**Input (getImageServingPublishSettingsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | The handle to the company with the image serving publish settings.  |
|  contextHandle  | `xsd:string`  | Yes  | Handle to the publish context.  |

**Output** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  publishSettingArray  | `xsd:string`  | Yes  | Array of image server publish settings.  |

