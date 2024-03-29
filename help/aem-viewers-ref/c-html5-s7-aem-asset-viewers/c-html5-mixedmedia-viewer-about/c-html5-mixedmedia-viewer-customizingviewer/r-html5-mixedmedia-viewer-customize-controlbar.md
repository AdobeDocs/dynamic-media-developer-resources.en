---
title: Control bar
description: The control bar is the rectangular area that contains and sits behind all the user interface controls available for the video viewer, such as the Play/Pause button, volume controls, and so on.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: f0de655c-36f0-4ed4-806c-d486eed2201b
---
# Control bar{#control-bar}

The control bar is the rectangular area that contains and sits behind all the user interface controls available for the video viewer, such as the Play/Pause button, volume controls, and so on.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

The control bar always takes the entire available viewer width. It is possible to change its color, height, and vertical position by CSS, relative to the video viewer container.

The following CSS class selector controls the appearance of the control bar:

```
.s7mixedmediaviewer .s7controlbar
```

## CSS properties of the control bar {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Height of the control bar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Background color of the control bar. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Example {#section-e8caea0a303c425a8a637c2a47c06355}

To set up a mixed media viewer with a gray control bar that is 30 pixels tall.

```
.s7mixedmediaviewer .s7controlbar {  
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
