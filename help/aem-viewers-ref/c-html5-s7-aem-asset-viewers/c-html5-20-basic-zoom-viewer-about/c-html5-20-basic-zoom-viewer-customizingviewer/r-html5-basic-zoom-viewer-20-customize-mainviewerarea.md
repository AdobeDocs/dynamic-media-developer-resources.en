---
description: The main view area is the area occupied by the zoom image. It usually sets to fit the available device screen when no size is specified.


solution: Experience Manager
title: Main viewer area

feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: f51de2d6-0de2-4a4d-bbf4-185547e6c550
---
# Main viewer area{#main-viewer-area}

The main view area is the area occupied by the zoom image. It usually sets to fit the available device screen when no size is specified.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS properties of the main viewer area**

The appearance of the viewing area is controlled with the following CSS class selector:

```
.s7basiczoomviewer
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

Example - to set up a viewer with white background ( `#FFFFFF`) and make its size 512 x 288 pixels.

```
.s7basiczoomviewer{ 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
