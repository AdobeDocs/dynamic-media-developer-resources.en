---
description: JavaScript API reference for eCatalog Viewer.


solution: Experience Manager
title: setParams

feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: cbd7987b-5e47-4ac0-8235-a217e5e6dee9
---
# setParams{#setparams}

JavaScript API reference for eCatalog Viewer.

 [!DNL ` setParams( *`params`*)`]

Sets one or more parameters to a given value. The method argument syntax is identical to a URL query string. That is, it represents name=value pairs separated with [!DNL `&`]. Just as in a query string, the names and values are percent-encoded using UTF8. Before you call [!DNL `init()`], this parameter must be called.

This method is optional if the viewer configuration information is passed with [!DNL `config`] JSON object to the constructor.

See also [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

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
<instance>.setParams("PageView.zoomstep=2,3&PageView.iscommand=op_sharpen%3d1")
```
