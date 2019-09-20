---
description: The full screen button causes the viewer to enter or exit full screen mode when clicked by the user. It is used when the viewer is displaying video and is located in the control bar. This button is not displayed if the viewer works in pop-up mode and the system does not support native full screen.
seo-description: The full screen button causes the viewer to enter or exit full screen mode when clicked by the user. It is used when the viewer is displaying video and is located in the control bar. This button is not displayed if the viewer works in pop-up mode and the system does not support native full screen.
seo-title: Video full screen button
solution: Experience Manager
title: Video full screen button
topic: Dynamic media
uuid: f264154b-eb4d-4dcb-b8c0-e06c383198ae
---

# Video full screen button{#video-full-screen-button}

The full screen button causes the viewer to enter or exit full screen mode when clicked by the user. It is used when the viewer is displaying video and is located in the control bar. This button is not displayed if the viewer works in pop-up mode and the system does not support native full screen.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

You can size, skin, and position the full screen button, relative to the control bar that contains it, by CSS.

The appearance of the full screen button is controlled with the CSS class selector:

```
.s7mixedmediaviewer .s7fullscreenbutton
```

**CSS properties of the full screen button**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Position from the top border, including padding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p> Position from the right border, including padding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p> Position from the left border, including padding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Position from the bottom border, including padding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> The width of the full screen button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>The height of the full screen button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> The displayed image for a given button state. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position inside artwork sprite, if CSS sprites are used. </p> <p>See <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>This button supports both the `state` and `selected` attribute selectors, which can be used to apply different skins to different button states. In particular, `selected='true'` corresponds to the "full screen" state and `selected='false'` corresponds to the "normal" state.

The button tool tip can be localized. See [Localization of user interface elements](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) for more information.

## Example {#section-e8caea0a303c425a8a637c2a47c06355}

To set up a full screen button that is 32 x 32 pixels, and positioned 6 pixels from the top and right edge of the control bar. Also, display a different image for each of the four different button states when selected or not selected.

```
.s7mixedmediaviewer . s7fullscreenbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='false'][state='up'] { 
background-image:url(images/enterFullBtn_up.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='false'][state='over'] {  
background-image:url(images/enterFullBtn_over.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='false'][state='down'] {  
background-image:url(images/enterFullBtn_down.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='false'][state='disabled'] { 
background-image:url(images/enterFullBtn_disabled.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='true'][state='up'] {  
background-image:url(images/exitFullBtn_up.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='true'][state='over'] {  
background-image:url(images/exitFullBtn_over.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='true'][state='down'] {  
background-image:url(images/exitFullBtn_down.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='true'][state='disabled'] {  
background-image:url(images/exitFullBtn_disabled.png); } 
}
```

