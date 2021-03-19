---
description: JavaScript API reference for Video Image Viewer.
seo-description: JavaScript API reference for Video Image Viewer.
seo-title: setAsset
solution: Experience Manager
title: setAsset
uuid: 8cb10b2e-addb-4659-a93b-5a53d0f8a5bb
feature: "Dynamic Media Classic,Viewers,SDK/API,Interactive Images"
role: "Developer,Business Practitioner"
---

# setAsset{#setasset}

JavaScript API reference for Video Image Viewer.

 ` setAsset( *`asset`*)`

Sets the new asset. You can call this parameter at any time, either before or after `init()`. If it is called after `init()`, the viewer swaps the asset at runtime.

See also [init](../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> asset</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} new asset ID. </p> <p>Images which use IR (Image Rendering) or UGC (User-Generated Content are not supported by this viewer. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

None.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Single image reference:

```
<instance>.setAsset("/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg")
```

