---
description: getVignettePublishFormats
solution: Experience Manager
title: getVignettePublishFormats
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6e56d68e-b5cf-4044-9c58-f8221fa4490f
TQID: 'https://experienceleague.adobe.com/2boU6c0m2JZ6kLBXvNVtb0udCXQAP4u8hrFIGk0Pezs'
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
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
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
|  companyHandle  | `xsd:string`  | Yes  | The handle to the company.  |

**Output (getVignettePublishFormatsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  vignetteFormatArray  | `types:VignettePublishFormatArray`  | Yes  | Array of vignette publish formats.  |

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

