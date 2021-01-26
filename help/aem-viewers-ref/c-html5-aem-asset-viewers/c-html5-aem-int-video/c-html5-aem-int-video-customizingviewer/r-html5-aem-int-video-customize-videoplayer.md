---
description: The video player is the rectangular area where the video content is displayed within the viewer.
seo-description: The video player is the rectangular area where the video content is displayed within the viewer.
seo-title: Video player
solution: Experience Manager
title: Video player
topic: Dynamic Media
uuid: ff0f78b1-ff88-47b8-a118-4e0b3e75f341
---

# Video player{#video-player}

The video player is the rectangular area where the video content is displayed within the viewer.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

If the dimensions of the video that is being played does not match the dimensions of the video player, the video content is centered within the video player's rectangle display area.

The following CSS class selector controls the appearance of the video player:

```
.s7interactivevideoviewer .s7videoplayer
```

**CSS properties of the video player**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Background color of the main view. </p> </td> 
  </tr> 
 </tbody> 
</table>

You can localize the error message that displayed in cases where the system is unable to play the video.

See [Localization of user interface elements](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Example - To set up a video viewer with the video player size set to 512 x 288 pixels.

```
.s7interactivevideoviewer .s7videoplayer{ 
background-color: transparent; 
}
```

Closed captions are put into an internal container inside the video player. The position of that container is controlled by supported WebVTT positioning operators. The caption text itself is inside that container, and its style is controlled with the following CSS class selector:

`.s7interactivevideoviewer .s7videoplayer .s7caption`

**CSS properties of closed captioning** 

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Closed caption text background. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Close caption text color. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p> Closed caption font weight. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p> Closed caption font size. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Closed caption font. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Example {#section-5b82913ff3c44b7b8187969cb15e9560}

To set up closed caption text to be 14 pixels, light gray, Arial, on a semi-transparent black background:

```
.s7interactivevideoviewer .s7videoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

The appearance of the buffering animation is controlled with the following CSS class selector:

```
.s7interactivevideoviewer .s7videoplayer .s7waiticon
```

**CSS properties of wait icon**

<table id="table_8DB41A0FF2A746F78B763564C4F3EBE0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS property </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Animation icon width. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Animation icon height. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p> Animation icon left margin, normally minus half of the icon's width. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> Animation icon top margin, normally minus half of the icon's height. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Knob artwork. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up a buffering animation to be 101 pixels wide, 29 pixels high:

```
.s7interactivevideoviewer .s7videoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```

