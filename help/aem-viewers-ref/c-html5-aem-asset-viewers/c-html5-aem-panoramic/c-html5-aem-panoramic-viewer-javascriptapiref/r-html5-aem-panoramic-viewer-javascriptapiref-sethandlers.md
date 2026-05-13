---
title: setHandlers
description: JavaScript API reference for Panoramic Viewer
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 90775d4a-386b-4b56-b75e-8afafe749645
TQID: 'https://experienceleague.adobe.com/BVnqG7dsjPf9ldhfOwTnByGvC6XyB-ASuvL--fNJEkE'
product_v2:
  - id: beaff0dd-a904-4c6b-8290-b527cd877d75
    internal-label: Dynamic Media Classic
---
# setHandlers{#sethandlers}

JavaScript API reference for Panoramic Viewer

 `setHandlers(handlers)`

Specifies zero or more callback handlers. A call to this method fully overwrites event handlers that were previously assigned for that viewer instance. Must be called before `init()`.

## Parameter {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> handlers </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> JSON object with viewer event callbacks, where the property name is the name of the supported viewer event and the property value is a JavaScript function reference to an appropriate callback. </p> <p>Refer to Event Callbacks section for more information about viewer events. </p> </td> 
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
