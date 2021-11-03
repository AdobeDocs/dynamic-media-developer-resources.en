---
description: The social share tool appears in the top right corner by default. It consists of a button and a panel which expands when user clicks or taps on a button and contains individual sharing tools.


solution: Experience Manager
title: Social share

feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 82b482f9-b117-4529-a422-cdb0eead0031
---
# Social share{#social-share}

The social share tool appears in the top right corner by default. It consists of a button and a panel which expands when user clicks or taps on a button and contains individual sharing tools.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

The position and size of the social share tool in the viewer user interface is controlled with the following:

```
.s7smartcropvideoviewer .s7socialshare
```

**CSS properties of the social share tool** 

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Vertical position of the social sharing tool relative to the viewer container. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p> Horizontal position of the social sharing tool relative to the viewer container. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> The width of the social sharing tool. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>The height of the social sharing tool. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - set up a social sharing tool that is positioned four pixels from the top and five pixels from the right of viewer container and is sized to 28 x 28 pixels.

```
.s7smartcropvideoviewer .s7socialshare { 
 top:4px; 
 right:5px; 
 width:28px; 
 height:28px; 
}
```

The appearance of the social share tool button is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7socialshare .s7socialbutton
```

**CSS properties of the social button** 

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> The image that is displayed for a given button state. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position inside artwork sprite, if CSS sprites are used. </p> <p>See <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>This button supports the `state` attribute selector, which can be used to apply different skins to different button states.

The button tool tip can be localized. See [Localization of user interface elements](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) for more information.

Example - set up a social sharing tool button that displays a different image for each of the four different button states.

```
.s7smartcropvideoviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7smartcropvideoviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7smartcropvideoviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7smartcropvideoviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

The appearance of the panel which contains the individual social sharing icons is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7socialshare .s7socialsharepanel
```

**CSS properties of the social share panel** 

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>The background color of the panel. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - set up a panel to have transparent color:

```
.s7smartcropvideoviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```
