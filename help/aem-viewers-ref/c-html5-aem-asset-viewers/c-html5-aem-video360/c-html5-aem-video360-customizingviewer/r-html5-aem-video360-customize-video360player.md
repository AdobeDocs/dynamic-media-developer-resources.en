---
description: The video player is the rectangular area where the video content is displayed within the viewer.
solution: Experience Manager
title: Video360 player
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 54ccf872-2d24-4d3f-9808-6d0e2558f5a5
---
# Video360 player{#video-player}

The video player is the rectangular area where the video content is displayed within the viewer.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

If the dimensions of the video that is being played does not match the dimensions of the video player, the video content is centered within the video player's rectangle display area.

The following CSS class selector controls the appearance of the video player:

```
.s7video360viewer .s7video360player
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

You can localize the error message that is displayed in cases where the system is unable to play the video.

See [Localization of user interface elements](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

Example - To set up a video viewer with the video player size set to 512 x 288 pixels.

```
.s7video360viewer .s7video360player{ 
background-color: transparent; 
}
```

<!--<a id="section_5B82913FF3C44B7B8187969CB15E9560"></a>-->

The appearance of the buffering animation is controlled with the following CSS class selector:

```
.s7video360viewer .s7video360player .s7waiticon
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
.s7video360viewer .s7video360player .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
