---
description: Configuration attribute for Video Viewer.
seo-description: Configuration attribute for Video Viewer.
seo-title: VideoPlayer.posterimage
solution: Experience Manager
title: VideoPlayer.posterimage
uuid: 59d81a72-ac17-4c32-ab47-89bd14dc17a5
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,Business Practitioner
---

# VideoPlayer.posterimage{#videoplayer-posterimage}

Configuration attribute for Video Viewer.

 ` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_id`*][? *`isCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> The image to display on the first frame before the video starts playing, resolved against <span class="codeph"> serverurl</span>. If specified in the URL, HTTP-encode the following: </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> as <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> as <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> as <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>If the <span class="codeph"><span class="varname"> image_id</span></span> value is omitted, the component attempts to use the default poster image for that asset instead. </p> <p>When the video is specified as a path, the default poster images catalog id is derived from the video path as the <span class="codeph"> catalog_id/image_id</span> pair where <span class="codeph"> catalog_id</span> corresponds to the first token in the path and <span class="codeph"> image_id</span> is the name of the video with the extension removed. If the image with that ID does not exist, the poster image is not shown. </p> <p>To prevent the display of the default poster image, specify <span class="codeph"> none</span> as the poster image value. If only the <span class="codeph"><span class="varname"> isCommands</span></span> are specified the commands are applied to the default poster image before the image is displayed. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Default {#section-d016470e92a74f98a18c4ab3489410a5}

None.

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
posterimage=none
```

