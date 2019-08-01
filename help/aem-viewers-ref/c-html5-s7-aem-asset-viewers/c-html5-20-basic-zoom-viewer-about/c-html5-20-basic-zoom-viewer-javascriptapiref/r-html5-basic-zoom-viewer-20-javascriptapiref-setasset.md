---
description: JavaScript API reference for Basic Zoom Viewer.
seo-description: JavaScript API reference for Basic Zoom Viewer.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: af433f15-34a0-4867-97c5-acab47e3e008
index: y
internal: n
snippet: y
---

# setAsset{#setasset}

JavaScript API reference for Basic Zoom Viewer.

 ` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> asset</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} new asset id, with optional IS modifiers appended after "?" </p> <p> Images that use IR (Image Rendering) or UGC (User-Generated Content) are not supported by this viewer. </p> </td> 
  </tr> 
 </tbody> 
</table>

Sets the new asset. You can call this parameter at any time, either before or after `init()`. If it is called after `init()`, the viewer swaps the asset at runtime.

See also [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

None.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Single image reference:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

Sharpening modifier added to all images in the set:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B?op_sharpen=1")
```

