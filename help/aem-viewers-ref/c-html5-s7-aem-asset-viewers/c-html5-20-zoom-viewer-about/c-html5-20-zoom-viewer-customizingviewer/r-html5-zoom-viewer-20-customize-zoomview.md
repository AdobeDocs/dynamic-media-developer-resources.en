---
title: Zoom view
description: Main view consists of the zoomable image.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ae6c7f6f-5d71-49b5-adbb-782520961acf
---
# Zoom view{#zoom-view}

Main view consists of the zoomable image.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS properties of the main viewer area**

The appearance of the viewing area is controlled with the following CSS class selector:

```
.s7zoomviewer .s7zoomview
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS property </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Background color in hexadecimal format of the main view. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor </span> </p> </td> 
   <td colname="col2"> <p>Cursor displayed over the main view. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - To make the main view transparent.

```
.s7zoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

On desktop systems the component supports `cursortype` attribute selector which can be applied to the `.s7zoomview` class. It controls the type of the cursor based on component state and user action. The following `cursortype` values are supported:

* `default`

  Displayed when the image is not zoomable because of a small image resolution, or component settings, or both. 

* `zoomin`

  Displayed when the image can be zoomed in. 

* `reset`

  Displayed when the image is at maximum zoom level and can be reset to its initial state. 

* `drag`

  Displayed when the user pans the image which is in zoomed in state. 

* `slide`

  Displayed when the user performs image swap by doing a horizontal swipe or flick.
