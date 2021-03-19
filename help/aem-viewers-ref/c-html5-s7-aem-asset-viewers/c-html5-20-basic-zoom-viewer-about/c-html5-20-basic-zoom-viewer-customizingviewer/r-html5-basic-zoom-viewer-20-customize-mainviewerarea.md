---
description: The main view area is the area occupied by the zoom image. It usually sets to fit the available device screen when no size is specified.
seo-description: The main view area is the area occupied by the zoom image. It usually sets to fit the available device screen when no size is specified.
seo-title: Main viewer area
solution: Experience Manager
title: Main viewer area
uuid: f37b8d25-4bd6-481e-88e7-98192186b177
feature: "Dynamic Media Classic,Viewers,SDK/API,Zoom"
role: "Developer,Business Practitioner"
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

