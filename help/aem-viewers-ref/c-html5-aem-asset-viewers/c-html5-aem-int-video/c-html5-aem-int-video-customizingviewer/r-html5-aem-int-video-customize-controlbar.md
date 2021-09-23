---
title: Control bar
description: The control bar is the rectangular area that contains and sits behind all the user interface controls that are available for the video viewer, such as the play/pause button and volume controls.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 685fad5a-a75a-4c0c-9038-de99d814f4be
---
# Control bar{#control-bar}

The control bar is the rectangular area that contains and sits behind all the user interface controls that are available for the video viewer, such as the play/pause button and volume controls.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

The control bar always takes the entire available viewer width. It is possible to change its color, height, and vertical position by CSS, relative to the video viewer container.

The following CSS class selector controls the appearance of the control bar:

```
.s7interactivevideoviewer .s7controlbar
```

## CSS properties of the control bar {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Position from the top border, including padding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p> Position from the bottom border, including padding. </p> </td> 
  </tr> 
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

To set up a video viewer with a gray control bar that is 30 pixels tall and sits at the top of the video viewer container.

```
.s7interactivevideoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
