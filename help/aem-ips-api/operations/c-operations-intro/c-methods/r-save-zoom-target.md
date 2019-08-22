---
description: Create or edit a zoom target.
seo-description: Create or edit a zoom target.
seo-title: saveZoomTarget
solution: Experience Manager
title: saveZoomTarget
topic: Scene7 Image Production System API
uuid: 161053be-9d89-4e87-a707-21a9184a3816
index: y
internal: n
snippet: y
---

# saveZoomTarget{#savezoomtarget}

Create or edit a zoom target.

 Syntax 

## Authorized User Type {#section-823cd9f0557045bca51da66768b5ba74}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-4a23983cae4e49a098e9bbe736933996}

**Input (saveZoomTargetParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company with the zoom target you want to save.  |
|  ` *`assetHandle`*`  | `xsd:string`  | Yes  | The handle to the zoom target.  |
|  ` *`zoomTargetHandle`*`  | `xsd:string`  | No  | Edits or creates a zoom target.  |
|  ` *`name`*`  | `xsd:string`  | Yes  | Zoom target name.  |
|  ` *`xPosition`*`  | `xsd:int`  | Yes  | Left pixel location.  |
|  ` *`yPosition`*`  | `xsd:int`  | Yes  | Top pixel location.  |
|  ` *`width`*`  | `xsd:int`  | Yes  | Zoom target width.  |
|  ` *`height`*`  | `xsd:int`  | Yes  | Zoom target height.  |
|  ` *`userData`*`  | `xsd:string`  | Yes  | For customer-specific information. Can contain any type of data.  |

**Output (saveZoomTargetReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`zoomTargetHandle`*`  | `xsd:string`  | Yes  | Handle to the newly created zoom target.  |

## Examples {#section-509c472c316549cdb228d7e1cfa8400a}

This code sample saves a zoom target. The response returns the zoom target handle.

**Request** 

```java
<saveZoomTargetParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>24267|1|17063</assetHandle>
   <name>My Zoom Target</name>
   <xPosition>2</xPosition>
   <yPosition>2</yPosition>
   <width>10</width>
   <height>10</height>
   <userData>My User Data</userData>
</saveZoomTargetParam>
```

**Response** 

```java
<saveZoomTargetReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <zoomTargetHandle>34194|9|301</zoomTargetHandle>
</saveZoomTargetReturn>
```

