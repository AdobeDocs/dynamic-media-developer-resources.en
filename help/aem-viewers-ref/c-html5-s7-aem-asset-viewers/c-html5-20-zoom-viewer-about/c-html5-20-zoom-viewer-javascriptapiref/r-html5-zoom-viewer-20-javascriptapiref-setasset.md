---
title: setAsset
description: JavaScript API reference for Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 4fc94f30-e330-4c8a-b6da-d870e4f8e4ab
---
# setAsset{#setasset}

JavaScript API reference for Video Viewer.

 ` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> asset </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>} new asset id, explicit image set, or explicit image set with frame-specific Image Serving modifiers, with optional global Image Serving modifiers appended after "?". </p> <p> Images which use IR (Image Rendering) or UGC (User-Generated Content) are not supported by this viewer. </p> </td> 
  </tr> 
 </tbody> 
</table>

Sets the new asset. You can call this parameter at any time, either before or after `init()`. If it is called after `init()`, the viewer swaps the asset at runtime.

See also [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

None.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Single image reference as follows:

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

Single reference to an image set that is defined in a catalog as follows:

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

Explicit image set as follows:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

Explicit image set with frame-specific Image Serving modifiers as follows:

```
 <instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

Sharpening modifier added to all images in the set as follows:

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample?op_sharpen=1")
```
