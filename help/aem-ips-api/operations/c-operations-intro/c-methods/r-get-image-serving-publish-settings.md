---
description: For internal use only. Users should refer to the Image Serving Image Catalog Reference – Attribute Reference section.
solution: Experience Manager
title: getImageServingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ab7b5df6-58fb-4111-be9c-76901534d167
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
