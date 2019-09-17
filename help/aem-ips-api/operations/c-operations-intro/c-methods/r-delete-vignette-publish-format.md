---
description: Deletes a vignette publish format.
seo-description: Deletes a vignette publish format.
seo-title: deleteVignettePublishFormat
solution: Experience Manager
title: deleteVignettePublishFormat
topic: Scene7 Image Production System API
uuid: 3c8148d5-dec6-4ffa-8ab8-2cd70811ada6
---

# deleteVignettePublishFormat{#deletevignettepublishformat}

Deletes a vignette publish format.

 Syntax 

## Authorized User Types {#section-a127680d6b53462daaf2579d6f6fe5a8}

****

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-789625ba29df4b5f880914d4c64f77ce}

**Input (deleteVignettePublishFormatParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company to which the vignette belongs.  |
|  ` *`vignetteFormatHandle`*`  | `xsd:string`  | Yes  | The handle to the vignette publish format to be deleted.  |

**Output (deleteVignettePublishFormatParam)**

The IPS API does not return a response for this operation.

## Examples {#section-5ab2a314ad4c41ac8b3a24eaea7d8585}

This code sample deletes a vignette publish format specified by its handle.

**Request** 

```java
<deleteVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</deleteVignettePublishFormatParam>
```

**Response**

None. 
