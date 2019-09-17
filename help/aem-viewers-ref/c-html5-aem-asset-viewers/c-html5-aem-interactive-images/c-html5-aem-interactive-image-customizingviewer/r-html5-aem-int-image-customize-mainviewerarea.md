---
description: The main view area is the area occupied by the zoom image. It is usually set to fit the available device screen when no size is specified.
seo-description: The main view area is the area occupied by the zoom image. It is usually set to fit the available device screen when no size is specified.
seo-title: Main viewer area
solution: Experience Manager
title: Main viewer area
topic: Dynamic media
uuid: 666328fe-1819-43a6-a2c2-ba63ac798700
---

# Main viewer area{#main-viewer-area}

The main view area is the area occupied by the zoom image. It is usually set to fit the available device screen when no size is specified.

<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>

**CSS properties of the main viewer area**

The appearance of the viewing area is controlled with the following CSS class selector:

```
.s7interactiveimage
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

Example - to set up a viewer with a white background ( `#FFFFFF`) and make its size 1174 x 500 pixels.

```
.s7interactiveimage { 
 background-color: #FFFFFF; 
 width: 1174px; 
 height: 500px;  
}
```

