---
title: PanoramicView.iscommand
description: Configuration attribute for Panoramic Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id:
---
# PanoramicView.iscommand{#panoramicview-iscommand}

Configuration attribute for Panoramic Viewer.

 ` [PanoramicView.|<containerId>_panoramicView.]iscommand=isCommand `

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> The Image Serving command string that is applied to the image.  If it is specified in the URL, be sure that you HTTP-encode all occurrences of <span class="codeph"> &amp;</span> and <span class="codeph"> =</span> as <span class="codeph"> %26</span> and <span class="codeph"> %3D</span>, respectively. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Properties {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Default {#section-d016470e92a74f98a18c4ab3489410a5}

No default.

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

When specified in the viewer URL.

```
iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000
```

When specified in the config data.

```
iscommand=op_sharpen=1&op_colorize=0xff0000
```
