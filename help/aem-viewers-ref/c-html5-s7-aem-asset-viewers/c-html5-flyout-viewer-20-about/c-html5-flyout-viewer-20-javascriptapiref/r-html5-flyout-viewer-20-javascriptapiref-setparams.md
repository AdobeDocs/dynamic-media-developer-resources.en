---
description: JavaScript API reference for Flyout Viewer.
seo-description: JavaScript API reference for Flyout Viewer.
seo-title: setParams
solution: Experience Manager
title: setParams
uuid: 12a513d3-32a9-411d-965f-f0eaf553d98d
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,Business Practitioner
---

# setParams{#setparams}

JavaScript API reference for Flyout Viewer.

 ` setParams( *`params`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value parameter pairs separated with <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Sets one or more parameters to a given value. The method argument syntax is identical to a URL query string. That is, it represents name=value pairs separated with `&`. The same as in a query string, names and values are percent-encoded using UTF8. Before you call `init()`, this parameter must be called. This method is optional if viewer configuration information is passed with `config` JSON object to the constructor.

See also [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

None.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("FlyoutZoomView.zoomfactor=2,3&Swatches.iscommand=op_sharpen%3d1")
```

