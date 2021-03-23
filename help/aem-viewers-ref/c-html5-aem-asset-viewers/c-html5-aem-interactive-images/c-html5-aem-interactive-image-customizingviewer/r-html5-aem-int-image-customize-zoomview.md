---
description: Main view consists of the static image.


solution: Experience Manager
title: Zoom view

feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,Business Practitioner
---

# Zoom view{#zoom-view}

Main view consists of the static image.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS properties of the main viewer area**

The appearance of the viewing area is controlled with the following CSS class selector:

```
.s7interactiveimage .s7zoomview
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
 </tbody> 
</table>

Example - to make the main view transparent.

```
.s7interactiveimage .s7zoomview { 
 background-color: transparent; 
}
```

