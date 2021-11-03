---
title: Main viewer area
description: The main view area is occupied by the smart crop video. It usually sets to fit the available device screen when no size is specified.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 7d1379c1-7746-4f61-92df-e8ac4ab7d506
---
# Main viewer area{#main-viewer-area}

The main view area is occupied by the video. It usually sets to fit the available device screen when no size is specified.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

The following CSS class selector controls the appearance of the viewing area:

```
.s7smartcropvideoviewer 
```

## CSS properties of the main viewer area {#css-properties-of-the-main-viewer-area}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Viewer width. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Viewer height. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Background color in hexadecimal format. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Example {#section-e8caea0a303c425a8a637c2a47c06355}

To set up a smart crop video viewer with a white background (#FFFFFF) and make its size 512 x 288 pixels:

```
.s7smartcropvideoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
