---
description: Sets the zoom target associated with an asset image. It overwrites existing zoom targets.
solution: Experience Manager
title: setZoomTargets
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1b4ac729-00cf-4ea2-9098-60b4af3c7e6d
---
# setZoomTargets{#setzoomtargets}

Sets the zoom target associated with an asset image. It overwrites existing zoom targets.

 Syntax 

## Authorizied User Types {#section-c5e1863e9cb1426591bfea513620b6ab}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-161f8c733cc4439f94a06e12119d4226}

**Input (setZoomTargetsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | Company handle.  |
|  assetHandle  | `xsd:string`  | Yes  | Asset with the zoom target you want to set.  |
|  zoomTargetArray  | `types:ZoomTargetDefinitionArray`  | Yes  | Array of zoom target definitions.  |

**Output (setZoomTargetsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  zoomTargetHandleArray  | `types:HandleArray`  | Yes  | The set of handles to the zoom targets created by this operation.  |

## Examples {#section-a2f14c7a1499443e96d099ea8a76c182}

This code sample defines an array of zoom targets by name, position (x and y axis), width, height, and assigns the array to an asset. The response contains handles to the newly created zoom targets.

**Request** 

```java
<setZoomTargetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <zoomTargetArray>
      <items>
         <name>zoomTarget2</name>
         <xPosition>40</xPosition>
         <yPosition>40</yPosition>
         <width>400</width>
         <height>400</height>
      </items>
      <items>
         <name>zoomTarget3</name>
         <xPosition>40</xPosition>
         <yPosition>40</yPosition>
         <width>400</width>
         <height>400</height>
      </items>
   </zoomTargetArray>
</setZoomTargetsParam>
```

**Response** 

```java
<setZoomTargetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <zoomTargetHandleArray>
      <items>a|947|9|41</items>
      <items>a|948|9|42</items>
   </zoomTargetHandleArray>
</setZoomTargetsReturn>
```
