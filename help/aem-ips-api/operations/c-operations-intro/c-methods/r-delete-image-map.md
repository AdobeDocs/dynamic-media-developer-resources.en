---
description: Deletes an image map.
seo-description: Deletes an image map.
seo-title: deleteImageMap
solution: Experience Manager
title: deleteImageMap
topic: Scene7 Image Production System API
uuid: b02d0696-e437-4a0c-a906-6caaf45eb9bf
index: y
internal: n
snippet: y
---

# deleteImageMap{#deleteimagemap}

Deletes an image map.

 Syntax 

## Authorized User Types {#section-41fd188af16a40d4b07923165bcf15d8}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

>[!NOTE]
>
>The user must have read and write access to the asset.

## Parameters {#section-28de12bab79045a5977c68855e37ae3d}

**Input (deleteImageMapParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company that contains the image map to delete.  |
|  ` *`imageMapHandle`*`  | `xsd:string`  | Yes  | The handle to the image map to delete.  |

**Output (deleteImageMapParam)**

The IPS API does not return a response for this operation.

## Examples {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

This code sample deletes an image map from a company. You must obtain the image map handle from another operation.

**Request** 

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**Response**

None 
