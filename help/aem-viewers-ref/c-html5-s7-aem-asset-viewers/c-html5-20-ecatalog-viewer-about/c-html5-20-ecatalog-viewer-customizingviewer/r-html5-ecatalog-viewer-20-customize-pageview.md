---
description: Main view consists of the catalog image. It can be swiped to get to another page or zoomed.


solution: Experience Manager
title: Page view

feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
exl-id: d3368115-15e7-4d9d-a417-a3c82c9a8a64
---
# Page view{#page-view}

Main view consists of the catalog image. It can be swiped to get to another page or zoomed.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS properties of the main viewer area**

The appearance of the viewing area is controlled with the following CSS class selector:

```
.s7ecatalogviewer .s7pageview
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
   <td colname="col2"> <p> Background color of the main view in hexadecimal format. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor </span> </p> </td> 
   <td colname="col2"> <p>Cursor that is displayed over the main view. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to make the main view transparent.

```
.s7ecatalogviewer .s7pageview { 
 background-color: transparent; 
}
```

On desktop systems the component supports the `cursortype` attribute selector which can be applied to `.s7pageview` class and controls the type of the cursor based on component state and user action. The following `cursortype` values are supported:

<table id="table_45B83F6CCDE84C36B0E087CA9144BFE6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Value </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> default </span> </p> </td> 
   <td colname="col2"> <p>Displayed when the image is not zoomable because of a small image resolution, component settings, or both. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin </span> </p> </td> 
   <td colname="col2"> <p>Displayed when the image can be zoomed in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reset </span> </p> </td> 
   <td colname="col2"> <p>Displayed when the image is at maximum zoom level and can be reset to initial state. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> drag </span> </p> </td> 
   <td colname="col2"> <p>Displayed when user pans the image which is in zoomed in state. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide </span> </p> </td> 
   <td colname="col2"> <p>Displayed when the user performs an image swap by doing horizontal swipe or flick. </p> </td> 
  </tr> 
 </tbody> 
</table>

The page divider that visually separates the left and right pages of the catalog spread is controlled with the following CSS class selector:

`.s7ecatalogviewer .s7pageview .s7pagedivider`

<table id="table_77EBC9A77BF14CF4974F8F43C709A207"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS property </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> The width of page divider. Set to <span class="codeph"> 0 </span> px to hide the divider completely. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>The image that you want to use as the page divider. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to have 40 pixels wide page divider with semi-transparent image.

```
.s7ecatalogviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>When the `frametransition` modifier is set to `turn` or `auto` (on desktop systems), the appearance of the page divider is controlled with the `pageturnstyle` modifier and the `.s7pagedivider` CSS class is ignored.

It is possible to configure the display of the custom mouse cursors over the main viewer area. This is controlled with the additional attribute selectors applied to `.s7ecatalogviewer .s7pageview` CSS class:

<table id="table_908164DECF9347A19A9696A23BBDB1A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS property </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> default </span> </p> </td> 
   <td colname="col2"> <p> Normally an arrow, displays for non-zoomable image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin </span> </p> </td> 
   <td colname="col2"> <p> Shows when an image can be zoomed in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reset </span> </p> </td> 
   <td colname="col2"> <p>Shows when an image is at maximum zoom and can be reset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> drag </span> </p> </td> 
   <td colname="col2"> <p>Shows when user performs drag operation on zoomed in image </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide </span> </p> </td> 
   <td colname="col2"> <p>Shows when user performs image swap using slide gesture </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - have different mouse cursors for each type of component state.

```
.s7ecatalogviewer .s7pageview[cursortype="default"] { 
cursor:auto; 
} 
.s7ecatalogviewer .s7pageview[cursortype="zoomin"] { 
cursor:url(images/zoomin_cursor.cur), auto; 
} 
.s7ecatalogviewer .s7pageview[cursortype="reset"] { 
cursor:url(images/zoomout_cursor.cur), auto; 
} 
.s7ecatalogviewer .s7pageview [cursortype="slide"] { 
cursor:url(images/slide_cursor.cur), auto; 
} 
.s7ecatalogviewer .s7pageview[cursortype="drag"] { 
cursor:url(images/drag_cursor.cur), auto; 
}
```
