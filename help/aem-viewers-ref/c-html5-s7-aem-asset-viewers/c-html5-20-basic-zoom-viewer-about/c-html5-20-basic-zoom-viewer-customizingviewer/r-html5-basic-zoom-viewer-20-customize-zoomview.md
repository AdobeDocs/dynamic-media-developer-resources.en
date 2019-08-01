---
description: Main view consists of the zoomable image.
seo-description: Main view consists of the zoomable image.
seo-title: Zoom view
solution: Experience Manager
title: Zoom view
topic: Dynamic media
uuid: 06464e36-8c9c-4d3c-b4e5-5911f002568c
index: y
internal: n
snippet: y
---

# Zoom view{#zoom-view}

Main view consists of the zoomable image.

<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>

**CSS properties of the main viewer area**

The appearance of the viewing area is controlled with the following CSS class selector:

```
.s7basiczoomviewer .s7zoomview
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
   <td colname="col2"> <p>Cursor is displayed over the main view. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to make the main view transparent.

```
.s7basiczoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

On desktop systems the component supports the `cursortype` attribute selector which can be applied to the `.s7zoomview` class and controls the cursor type based on the component state and user action. The following `cursortype` values are supported:

<table id="table_BC9FC40DA27B4A85995F4E9431AABF33"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Value </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> default </span> </p> </td> 
   <td colname="col2"> <p>Displayed when the image is not zoomable because of a small image resolution, or component settings, or both. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin </span> </p> </td> 
   <td colname="col2"> <p>Displayed when the image can be zoomed in on. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reset </span> </p> </td> 
   <td colname="col2"> <p>Displayed when the image is at maximum zoom level and can be reset to its initial state. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> drag </span> </p> </td> 
   <td colname="col2"> <p>Displayed when a user pans the image which is in zoomed in state. </p> </td> 
  </tr> 
 </tbody> 
</table>

