---
title: Video player icon effect
description: The Play icon is overlaid on the video view area. It displays when the video is paused, or when the end of the video is reached, and it also depends on the iconeffect parameter.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1e0bd97f-20e9-41e6-95fc-d693644152da
TQID: https://experienceleague.adobe.com/SO7Stm6DNmYfjWffRWM2ZJXS49gGyALfAnlcLUQ5-0E
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# Video player icon effect{#video-player-icon-effect}

The Play icon is overlaid on the video view area. It displays when the video is paused, or when the end of the video is reached, and it also depends on the iconeffect parameter.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

The appearance of the play icon is controlled with the following CSS class selector:

```
.s7mixedmediaviewer . s7videoplayer .s7iconeffect
```

**CSS properties of the play icon**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> The displayed image for the play icon. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position inside artwork sprite, if CSS sprites are used. </p> <p>See <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> The width of the play icon. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>The height of the play icon. </p> </td> 
  </tr> 
 </tbody> 
</table>

Icon effect supports the `state` attribute selector. The selector `state="play"` is used when the video is paused in the middle of playback, and `state="replay"` is used when the play head is in the end of the stream.

## Example {#section-e8caea0a303c425a8a637c2a47c06355}

Set up a 100 x 100 pixel play icon.

```
.s7mixedmediaviewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7mixedmediaviewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7mixedmediaviewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```
