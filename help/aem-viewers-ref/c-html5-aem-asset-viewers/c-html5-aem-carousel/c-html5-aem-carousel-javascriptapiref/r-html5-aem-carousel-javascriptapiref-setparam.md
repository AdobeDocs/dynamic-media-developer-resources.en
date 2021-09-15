---
title: setParam
description: JavaScript API reference for Carousel Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 0829933f-a90b-4066-9904-748f2a727169
---
# setParam{#setparam}

JavaScript API reference for Carousel Viewer.

 ` setParam( *`name, value`*)`

Sets the viewer parameter to a specified value. The parameter is either a viewer-specific configuration option or a software development kit modifier. This parameter is called before `init()`.

This method is optional if the viewer configuration information was passed with `config` JSON object to constructor.

See also [xref](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md).

## Parameters {#section-c68a5a3688d342fd9d6a7fd59867cc7a}

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
<instance>.setParam("style", "etc/dam/presets/css/html5_carouselviewer_dotted_light.css")
```
