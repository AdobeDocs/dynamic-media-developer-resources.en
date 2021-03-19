---
description: JavaScript API reference for Video Viewer.
seo-description: JavaScript API reference for Video Viewer.
seo-title: setHandlers
solution: Experience Manager
title: setHandlers
uuid: 02535997-521f-420f-af0b-5c8ec0fe0876
feature: "Dynamic Media Classic,Viewers,SDK/API,Video"
role: "Developer,Business Practitioner"
---

# setHandlers{#sethandlers}

JavaScript API reference for Video Viewer.

 `setHandlers(handlers)`

Specifies zero or more callback handlers. A call to this method fully overwrites event handlers that were previously assigned for that viewer instance. Must be called before `init()`.

## Parameter {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> handlers </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> JSON object with viewer event callbacks, where the property name is the name of the supported viewer event and the property value is a JavaScript function reference to an appropriate callback. </p> <p>See <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-event-callbacks.md#concept-ebe5a4c1853d4912a919d86df35c1f6d" format="dita" scope="local"> Event callbacks </a> for more information about viewer events. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

None.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
})
```

