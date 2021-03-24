---
description: Deletes an image format. Get the image format handle from saveImageFormat.
solution: Experience Manager
title: deleteImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
---

# deleteImageFormat{#deleteimageformat}

Deletes an image format. Get the image format handle from saveImageFormat.

 Syntax 

## Authorized User Types {#section-827e24a3019543418b0a635d46c1edfd}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-462c05d9aad746ee8d2be0656041b693}

**Input (deleteImageFormatParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company that contains the image format that you want to delete.  |
|  `*`imageFormatHandle`*`  | `xsd:string`  | Yes  | The handle to the image format you want to delete.  |

**Output (deleteImageFormatParam)**

The IPS API does not return a response for this operation.

## Examples {#section-9ed9baaba13549bfaad1bc9cd7ec7009}

This code sample deletes an image format from a company. Obtain the image format handle from another operation.

**Request** 

```java
<deleteImageFormatParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageFormatHandle>47|301</imageFormatHandle>
</deleteImageFormatParam>
```

**Response**

None.

**Related Topic:**

[saveImageFormat](../../../operations/c-operations-intro/c-methods/r-save-image-format.md#reference-d15c27f533ef41e38b54a539a304bd1d) 
