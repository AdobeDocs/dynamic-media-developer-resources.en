---
description: getVignettePublishFormats
solution: Experience Manager
title: getVignettePublishFormats
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
---

# getVignettePublishFormats{#getvignettepublishformats}

 Syntax 

## Authorizied User Types {#section-1f5e2f74aef8408e89ed9ccac8b5b9bc}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-ba28150e6d8c4aa0b4ec72451ba7bc71}

**Input (getVignettePublishFormatsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company.  |

**Output (getVignettePublishFormatsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`vignetteFormatArray`*`  | `types:VignettePublishFormatArray`  | Yes  | Array of vignette publish formats.  |

## Examples {#section-2cc32b27cc6243b7b3e273cc05996226}

This code sample returns two vignette publish formats associated with a specific company. Information is returned in an array, which is truncated for brevity.

**Request** 

```java
<getVignettePublishFormatsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
</getVignettePublishFormatsParam>
```

**Response** 

```java
<getVignettePublishFormatsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatArray>
      <items>
         <companyHandle>c|21</companyHandle>
         <vignetteFormatHandle>v|21|281</vignetteFormatHandle>
         <name>APIcreateVignettePublishFormat</name>
         ...
      </items>
   </vignetteFormatArray>
</getVignettePublishFormatsReturn>
```

