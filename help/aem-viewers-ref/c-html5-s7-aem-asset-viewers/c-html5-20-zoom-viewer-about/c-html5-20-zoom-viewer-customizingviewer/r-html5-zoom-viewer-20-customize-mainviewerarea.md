---
description: The main view area is the area occupied by the zoom image and swatches. It usually sets to fit the available device screen when no size is specified.
seo-description: The main view area is the area occupied by the zoom image and swatches. It usually sets to fit the available device screen when no size is specified.
seo-title: Main viewer area
solution: Experience Manager
title: Main viewer area
topic: Dynamic media
uuid: 689116cb-bbb9-4e26-9c16-9229330c4034
index: y
internal: n
snippet: y
---

# Main viewer area{#main-viewer-area}

The main view area is the area occupied by the zoom image and swatches. It usually sets to fit the available device screen when no size is specified.

<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>

When working in embedded mode (when an explicit size is given to the main viewer area), the viewer automatically decreases the height of its main area by the height of Swatches component that is in working with the single image and therefore, swatches are not needed.

**CSS properties of the main viewer area**

The appearance of the viewing area is controlled with the following CSS class selector:

```
.s7zoomviewer
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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>The width of the viewer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>The height of the viewer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Background color in hexadecimal format. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up a viewer with a white background ( `#FFFFFF`) and make its size 512 x 288 pixels.

```
.s7zoomviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

