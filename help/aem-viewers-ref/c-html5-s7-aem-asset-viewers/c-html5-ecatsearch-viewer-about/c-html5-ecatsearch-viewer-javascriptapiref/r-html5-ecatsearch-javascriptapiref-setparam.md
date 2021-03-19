---
description: JavaScript API reference for eCatalog Viewer.
seo-description: JavaScript API reference for eCatalog Viewer.
seo-title: setParam
solution: Experience Manager
title: setParam
uuid: a732461f-1b34-4ebe-9dfd-69175762e574
feature: "Dynamic Media Classic,Viewers,SDK/API,eCatalog Search"
role: "Developer,Business Practitioner"
---

# setParam{#setparam}

JavaScript API reference for eCatalog Viewer.

 [!DNL ` setParam( *`name, value`*)`]

Sets the viewer parameter to a specified value. The parameter is either a viewer-specific configuration option or a software development kit modifier. This parameter is called before [!DNL `init()`].

This method is optional if the viewer configuration information is passed with [!DNL `config`] JSON object to the constructor.

See also [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

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
[!DNL <instance>.setParam("style", "customStyle.css")]
```

