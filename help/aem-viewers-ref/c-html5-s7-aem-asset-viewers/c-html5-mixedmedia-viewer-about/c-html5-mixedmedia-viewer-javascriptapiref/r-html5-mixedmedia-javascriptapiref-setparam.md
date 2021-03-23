---
description: JavaScript API reference for Mixed Media Viewer.


solution: Experience Manager
title: setParam

feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
---

# setParam{#setparam}

JavaScript API reference for Mixed Media Viewer.

 ` setParam( *`name, value`*)`

Sets the viewer parameter to a specified value. The parameter is either a viewer-specific configuration option or a software development kit modifier. This parameter is called before `init()`. This method is optional if viewer configuration information is passed with `config` JSON object to the constructor.

See also [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

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

