---
description: Creates a preset view that determines what a user can see. The viewer can be of any type available in IPS. The preset view is applied when the assets are published.
seo-description: Creates a preset view that determines what a user can see. The viewer can be of any type available in IPS. The preset view is applied when the assets are published.
seo-title: createViewerPreset
solution: Experience Manager
title: createViewerPreset
uuid: 4160d2b0-6147-459f-830a-43c99b8dc196
feature: "Dynamic Media Classic,SDK/API,Viewer Presets"
role: "Developer,Administrator"
---

# createViewerPreset{#createviewerpreset}

Creates a preset view that determines what a user can see. The viewer can be of any type available in IPS. The preset view is applied when the assets are published.

 Syntax 

## Authorized User Types {#section-0b8b1322ebea4a7ea24d516e080b7367}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-aa6dc37e327541ebbfed7685cd8071ff}

**Input (createViewerPresetParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | The handle of the company that contains the viewer presets and assets.  |
|  `*`folderHandle`*`  | `xsd:string`  | Yes  | The handle of the folder that contains the assets.  |
|  `*`name`*`  | `xsd:string`  | Yes  | Viewer name.  |
|  `*`type`*`  | `xsd:string`  | Yes  | Viewer type.  |
|  `*`configSettingArray`*`  | `types:ConfigSettingArray`  | No  | An array that contains names, values, and handles of images that you're applying presets to.  |

**Output (createViewerPresetReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`viewerPresetHandle`*`  | `xsd:string`  | Yes  | Handle of the preset to the viewer.  |

## Examples {#section-c88ea63536f3461cbe4677ba53f875dd}

This code sample creates a video player preset. The response returns a handle to the preset.

```java
<createViewerPresetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|0</companyHandle>
   <folderHandle>Scene7SharedAssets/</folderHandle>
   <name>eVideo4</name>
   <type>VideoPlayer</type>
   <configSettingArray>
      <items>
         <name>Video Bit Rate</name>
         <value>393334.6508779093</value>
      </items>
      <items>
         <name>Audio Sample Rate</name>
         <value>44100</value>
      </items>
      ...
      <items>
         <name>vidPaneWidth</name>
         <value>0</value>
      </items>
   </configSettingArray>
</createViewerPresetParam>
```

**Response** 

```java
<createViewerPresetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <viewerPresetHandle>a|151760|40|151760</viewerPresetHandle>
</createViewerPresetReturn>
```

