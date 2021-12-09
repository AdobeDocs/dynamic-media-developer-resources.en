---
title: getComponent
description: JavaScript API reference for Panoramic Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 3c228b84-fbad-434f-96b4-d52485711844
---
# getComponent{#getcomponent}

JavaScript API reference for Panoramic Viewer

 `getComponent(componentId)`


Returns a reference to the Viewer SDK component that is used by the viewer. The web page can use this method to extend or customize the behavior of the out-of-box viewer. Call this method only after the `initComplete` viewer callback has run, otherwise the component may not be created yet by the viewer logic.

## Parameters {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*` - `{String}` an ID of the Viewer SDK component used by the viewer. This viewer supports the following component IDs:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Component ID </p> </th> 
   <th colname="col2" class="entry"> <p>Viewer SDK component class name </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> container </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> panoramicView </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.PanoramicView </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

When working with SDK APIs, it is important to use correct fully qualified SDK namespace as described in [Viewer SDK namespace](../../../c-html5-aem-asset-viewers/c-html5-aem-panoramic/c-html5-aem-panoramic-viewer-sdk-namespace.md#concept-4ee8657c7d67421f8e7880130a246621).

See the Viewer SDK API documentation for more information about a particular component.

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` a reference to Viewer SDK component. The method returns `null` if the `componentId` is not a supported viewer component or if the component was not yet created by the viewer logic.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var panoramicView = <instance>.getComponent("panoramicView"); 
} 
})
```
