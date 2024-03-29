---
description: Creates an image set.
solution: Experience Manager
title: createImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 01ccc705-97e4-4e75-a322-e24bb78cb496
---
# createImageSet{#createimageset}

Creates an image set.

 Syntax 

## Authorized User Types {#section-58bf5027e6d24ab5a9fcba59776d15dc}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

>[!NOTE]
>
>The user must have read/write access to the destination folder.

## Parameters {#section-03d22ba7d290477e91c25ca1d4439200}

**Input (createImageSetParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | The handle to the company that the image set belongs to.  |
|  folderHandle  | `xsd:string`  | Yes  | The handle to the folder.  |
|  name  | `xsd:string`  | Yes  | Image set name.  |
|  type  | `xsd:string`  | Yes  | Image set type.  |
|  thumbAssetHandle  | `xsd:string`  | No  | Handle of the asset that acts as the thumbnail for the new image set. If not specified, IPS tries to use the first image asset referenced by the set.  |

**Output** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  assetHandle  | `xsd:string`  | Yes  | The handle to the new image set.  |

## Examples {#section-385fe3b0af8044b0a2451336ec137fc5}

This code sample creates an image set specified by company, folder, name, and type. The response is an asset handle of the newly created image set.

**Request** 

```java
<ns1:createImageSetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/eCatalogs/</ns1:folderHandle>
   <ns1:name>My Image Set</ns1:name>
   <ns1:type>ImageSet</ns1:type>
</ns1:createImageSetParam>
```

**Response** 

```java
<createImageSetReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <assetHandle>25741|22|841</assetHandle>
</createImageSetReturn>

```
