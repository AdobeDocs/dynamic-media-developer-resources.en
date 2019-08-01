---
description: JavaScript API reference for Inline Zoom Viewer.
seo-description: JavaScript API reference for Inline Zoom Viewer.
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
topic: Dynamic media
uuid: 52f81748-d007-4f42-9057-7947cc02b231
index: y
internal: n
snippet: y
---

# setContainerId{#setcontainerid}

JavaScript API reference for Inline Zoom Viewer.

 ` setContainerId( *`containerId`*)`

Sets the ID of the DOM container (normally a `DIV`) into which the viewer is inserted. It is not necessary to have the container element created by the time this method is called. However, the container must exist when `init()` is run. It must be called before `init()`. This method is optional if viewer configuration information is passed with `config` JSON object to the constructor.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> ID of container. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

None.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```

