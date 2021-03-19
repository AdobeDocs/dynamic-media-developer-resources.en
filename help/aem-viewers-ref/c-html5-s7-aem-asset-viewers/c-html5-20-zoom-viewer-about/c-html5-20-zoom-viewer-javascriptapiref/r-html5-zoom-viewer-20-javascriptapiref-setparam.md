---
description: JavaScript API reference for Video Viewer.
seo-description: JavaScript API reference for Video Viewer.
seo-title: setParam
solution: Experience Manager
title: setParam
uuid: 7688134f-ab85-43ce-9ff8-9965bd33acd0
feature: "Dynamic Media Classic,Viewers,SDK/API,Zoom"
role: "Developer,Business Practitioner"
---

# setParam{#setparam}

JavaScript API reference for Video Viewer.

 ` setParam( *`name, value`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> name </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> name of parameter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> value of parameter. The value cannot be percent-encoded. </p> </td> 
  </tr> 
 </tbody> 
</table>

Sets the viewer parameter to a specified value. The parameter is either a viewer-specific configuration option or a software development kit modifier. This parameter is called before `init()`.

This method is optional if the viewer configuration information was passed with `config` JSON object to constructor.

See also [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

None.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```

