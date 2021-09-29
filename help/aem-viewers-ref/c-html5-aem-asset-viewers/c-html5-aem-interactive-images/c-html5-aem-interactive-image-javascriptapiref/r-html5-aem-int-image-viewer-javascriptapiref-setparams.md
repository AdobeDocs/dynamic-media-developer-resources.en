---
title: setParams
description: JavaScript API reference for Video Image Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 6a09e3bc-e79c-4206-be42-0c6ae3d91590
---
# setParams{#setparams}

JavaScript API reference for Video Image Viewer.

 ` setParams( *`params`*)`

Sets one or more parameters to a given value. The method argument syntax is identical to a URL query string. That is, it represents name=value pairs separated with `&`. In a query string, the names and values are percent-encoded using UTF8. Before you call `init()`, this parameter must be called.

This method is optional if the viewer configuration information was passed with `config` JSON object to constructor.

See also [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Parameter {#section-add05f3d7ca0426897bd74bf7ac9b9cd}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value parameter pairs separated with <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

None.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("ZoomView.fmt=png&ZoomView.iscommand=op_sharpen%3d1")
```
