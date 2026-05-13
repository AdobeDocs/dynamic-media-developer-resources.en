---
title: Main viewer area
description: The main view area is occupied by the smart crop video. It usually sets to fit the available device screen when no size is specified.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: c8ea6698-e425-491f-8413-2260ddf40c33
TQID: 'https://experienceleague.adobe.com/m3jZ1-S4Y-1fJJBKvCrrpPi2I9pFEchDMaGhRI-0yBM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
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
