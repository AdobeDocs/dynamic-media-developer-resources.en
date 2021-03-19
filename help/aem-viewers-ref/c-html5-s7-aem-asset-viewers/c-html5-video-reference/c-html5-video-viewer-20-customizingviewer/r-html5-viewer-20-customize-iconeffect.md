---
description: The play icon is overlaid on the main view area. It displays when the video is paused, or when the end of the video is reached, and it also depends on the iconeffect parameter.
seo-description: The play icon is overlaid on the main view area. It displays when the video is paused, or when the end of the video is reached, and it also depends on the iconeffect parameter.
seo-title: Icon effect
solution: Experience Manager
title: Icon effect
uuid: dcab487d-0bd6-4899-82e2-e29fa812a864
feature: "Dynamic Media Classic,Viewers,SDK/API,Video"
role: "Developer,Business Practitioner"
---

# Icon effect{#icon-effect}

The play icon is overlaid on the main view area. It displays when the video is paused, or when the end of the video is reached, and it also depends on the iconeffect parameter.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

The appearance of the play icon is controlled with the following CSS class selector:

```
.s7videoviewer . s7videoplayer .s7iconeffect
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
   <td colname="col2"> <p> Position inside artwork sprite, if CSS sprites are used. </p> <p>See <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
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

Icon effect supports the `state` attribute selector. `state="play"` is used when the video is paused in the middle of playback, and `state="replay"` is used when the play head is in the end of the stream.

## Example {#section-e8caea0a303c425a8a637c2a47c06355}

Setup a 100 x 100 pixel play icon.

```
.s7videoviewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7videoviewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7videoviewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```

