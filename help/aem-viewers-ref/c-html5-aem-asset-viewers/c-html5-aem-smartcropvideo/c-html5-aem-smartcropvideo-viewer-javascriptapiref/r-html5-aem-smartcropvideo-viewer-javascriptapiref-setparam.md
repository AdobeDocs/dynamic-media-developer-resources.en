---
description: JavaScript API reference for Smart Crop Video Viewer.


solution: Experience Manager
title: setParam

feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: b28ffb51-1091-4f2e-b12d-904218daf117
---
# setParam{#setparam}

JavaScript API reference for Smart Crop Video Viewer.

 ` setParam( *`name, value`*)`

Sets the viewer parameter to a specified value. The parameter is either a viewer-specific configuration option or a software development kit modifier. This parameter is called before `init()`.

This method is optional if the viewer configuration information was passed with `config` JSON object to the constructor.

See also [init](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

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

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

None.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
