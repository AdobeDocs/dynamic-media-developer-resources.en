---
title: setAsset
description: JavaScript API reference for Panoramic Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 1fcd7dbe-d122-4501-92f4-3ce93a94a933
---
# setAsset{#setasset}

JavaScript API reference for Panoramic Viewer.

 `setAsset(asset)`

Sets the new asset. You can call this parameter at any time, either before or after `init()`. If it is called after `init()`, the viewer swaps the asset at runtime.

See also [init](../../../c-html5-aem-asset-viewers/c-html5-aem-panoramic/c-html5-aem-panoramic-viewer-javascriptapiref/r-html5-aem-panoramic-viewer-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> asset </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} new asset id. Images which use Image Rendering (IR) or User-Generated Content (UGC) are not supported by this viewer. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

None.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Scene7SharedAssets/PanoramicImage-Sample")
```
