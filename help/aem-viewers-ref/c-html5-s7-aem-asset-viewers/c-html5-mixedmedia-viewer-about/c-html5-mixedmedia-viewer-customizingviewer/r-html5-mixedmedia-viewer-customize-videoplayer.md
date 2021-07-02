---
description: The video player is the rectangular area where the video content is displayed within the viewer.
solution: Experience Manager
title: Video player
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,Business Practitioner
exl-id: 2f92d76e-3104-4ad8-9426-662275492251
---
# Video player{#video-player}

The video player is the rectangular area where the video content is displayed within the viewer.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

If the dimensions of the video that is being played does not match the dimensions of the video player, the video content is centered within the video player's rectangle display area.

The following CSS class selector controls the appearance of the video player:

```
.s7mixedmediaviewer .s7videoplayer
```

**CSS properties of the video player**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> The background color of the video player. </p> </td> 
  </tr> 
 </tbody> 
</table>

The error message that is displayed if the system is unable to play the video can be localized. See [Localization of user interface elements](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) for more information.

Example - To make the video player transparent:

```
.s7mixedmediaviewer .s7videoplayer { 
 background-color: transparent; 
}
```

Captions are put into internal container inside the video player. The position of that container is controlled by supported WebVTT positioning operators. The caption text itself is inside that container; its style is controlled with the following CSS class selector:

```
.s7mixedmediaviewer .s7videoplayer .s7caption
```

**CSS properties of captions**

<table id="table_5417B0C0343747649502629F43DF231A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS property </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Caption text background. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Caption text color. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Font weight. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Font size. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Font family. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - To set up caption text to be 14 pixel light gray Arial on a semi-transparent black background:

```
.s7mixedmediaviewer .s7videoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

The appearance of the buffering animation is controlled with the following CSS class selector:

```
.s7mixedmediaviewer .s7videoplayer .s7waiticon
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

Example - To set up a buffering animation to be 101 pixels wide, 29 pixels high:

```
.s7mixedmediaviewer .s7videoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
