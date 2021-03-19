---
description: JavaScript API reference for Mixed Media Viewer.
seo-description: JavaScript API reference for Mixed Media Viewer.
seo-title: setAsset
solution: Experience Manager
title: setAsset
uuid: 8c341a8a-25b5-4db9-ad1a-919ded79f2ed
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
---

# setAsset{#setasset}

JavaScript API reference for Mixed Media Viewer.

 ` setAsset( *`asset`*[,data]))`

Sets the new asset and optional additional asset data. You can call this parameter at any time, either before or after `init()`. If it is called after `init()`, the viewer swaps the asset at runtime.

See also [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Parameters {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`asset`*` - { `String`} new asset ID or explicit mixed media set, with optional Image Serving modifiers appended after `?`.

Images which use IR (Image Rendering) or UGC (User-Generated Content) are not supported by this viewer.

`*`data`*` - { `JSON`} location of the new caption file.

If not specified, the caption button is not visible in the user interface. Captions specified with this parameter apply to the video that comes first in the mixed media set; subsequent videos play without captions. This viewer supports the following component IDs:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Component ID </p> </th> 
   <th colname="col2" class="entry"> <p>Viewer SDK component class name </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posterimage </span> </p> </td> 
   <td colname="col2"> <p>Image to display on the first frame before the video starts playing. </p> <p>See <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-posterimage.md#reference-f424ad0f278b4d14b86ea55e3a73c52b" format="dita" scope="local"> VideoPlayer.posterimage </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> caption </span> </p> </td> 
   <td colname="col2"> <p> Location of the new caption file. </p> <p>If not specified, the caption button is not visible in the user interface. Captions specified with this parameter apply to the video that comes first in the media set. Subsequent videos play without captions. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

None.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Single media set reference:

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample")
```

Explicit media set:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;")
```

Sharpening modifier added to all images in the set:

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample?op_sharpen=1")
```

