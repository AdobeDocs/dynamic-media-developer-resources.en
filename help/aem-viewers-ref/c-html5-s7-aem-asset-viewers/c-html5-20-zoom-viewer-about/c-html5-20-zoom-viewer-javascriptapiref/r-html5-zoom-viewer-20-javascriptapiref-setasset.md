---
description: JavaScript API reference for Video Viewer.
seo-description: JavaScript API reference for Video Viewer.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic Media
uuid: f106b3d4-880e-4ba3-ae47-a005af5c0f1b
---

# setAsset{#setasset}

JavaScript API reference for Video Viewer.

 ` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> asset </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>} new asset id, explicit image set or explicit image set with frame-specific Image Serving modifiers, with optional global Image Serving modifiers appended after "?". </p> <p> Images which use IR (Image Rendering) or UGC (User-Generated Content) are not supported by this viewer. </p> </td> 
  </tr> 
 </tbody> 
</table>

Sets the new asset. You can call this parameter at any time, either before or after `init()`. If it is called after `init()`, the viewer swaps the asset at runtime.

See also [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

None.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Single image reference:

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

Single reference to an image set that is defined in a catalog:

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

Explicit image set:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

Explicit image set with frame-specific Image Serving modifiers:

```
 <instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

Sharpening modifier added to all images in the set:

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample?op_sharpen=1")
```

