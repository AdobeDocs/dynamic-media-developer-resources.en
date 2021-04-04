---
description: The secondary control bar is the rectangular area that contains First and Last Page buttons and a Page Indicator when made available in CSS.


solution: Experience Manager
title: Secondary control bar

feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
exl-id: 2354c3a0-2df7-4a18-aac1-fac158a9b659
---
# Secondary control bar{#secondary-control-bar}

The secondary control bar is the rectangular area that contains First and Last Page buttons and a Page Indicator when made available in CSS.

 By default, it is displayed on mobile phones only and is located in the bottom of the viewer. It always takes the whole available viewer width. It is possible to change its color, height and vertical position by CSS, relative to the viewer container.

The appearance of the secondary control bar is controlled with the following CSS class selector:

`.s7ecatalogviewer .s7secondarycontrols .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS property </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Position from the top of the viewer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Position from the bottom of the viewer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>The height of the main control bar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>The background color of the secondary control bar. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up a gray secondary control bar that is 72 pixels tall and is positioned at the bottom of the viewer container.

```
.s7ecatalogviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```
