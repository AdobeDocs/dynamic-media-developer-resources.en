---
description: For internal use only. Users should refer to the Image Serving Image Catalog Reference – Attribute Reference section.
seo-description: For internal use only. Users should refer to the Image Serving Image Catalog Reference – Attribute Reference section.
seo-title: getImageServingPublishSettings
solution: Experience Manager
title: getImageServingPublishSettings
topic: Scene7 Image Production System API
uuid: 2f00198d-0262-430b-8ac5-80f52adcff67
index: y
internal: n
snippet: y
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
|  ` *`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company with the image serving publish settings.  |
|  ` *`contextHandle`*`  | `xsd:string`  | Yes  | Handle to the publish context.  |

**Output** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`publishSettingArray`*`  | `xsd:string`  | Yes  | Array of image server publish settings.  |

