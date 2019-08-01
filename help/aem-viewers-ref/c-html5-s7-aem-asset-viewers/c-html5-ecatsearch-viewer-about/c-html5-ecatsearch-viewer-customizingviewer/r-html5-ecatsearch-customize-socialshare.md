---
description: The social share tool appears in the top left corner by default. It consists of a button and a panel which expands when user clicks or taps on a button and contains individual sharing tools.
seo-description: The social share tool appears in the top left corner by default. It consists of a button and a panel which expands when user clicks or taps on a button and contains individual sharing tools.
seo-title: Social share
solution: Experience Manager
title: Social share
topic: Dynamic media
uuid: 6d463eb1-c6bf-4f1c-90e4-b5ef1e5a1538
index: y
internal: n
snippet: y
---

# Social share{#social-share}

The social share tool appears in the top left corner by default. It consists of a button and a panel which expands when user clicks or taps on a button and contains individual sharing tools.

<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>

The position and size of the social share tool in the viewer user interface is controlled with the following:

```
.s7ecatalogsearchviewer .s7socialshare
```

**CSS properties of the social share tool** 

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> The offset from the top of the control bar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin=left </span> </p> </td> 
   <td colname="col2"> <p> The distance to the next button on the left, or the left side of the control bar if this is the first button in a row. </p> </td> 
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
.s7ecatalogsearchviewer .s7socialshare { 
margin-top: 4px; 
margin-left: 10px; width:28px; 
 height:28px; 
}
```

The appearance of the social share tool button is controlled with the following CSS class selector:

```
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton
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
   <td colname="col2"> <p> Position inside artwork sprite, if CSS sprites are used. </p> <p>See also <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>This button supports the `state` attribute selector, which can be used to apply different skins to different button states.

The button tool tip can be localized. See [Localization of user interface elements](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) for more information.

Example - set up a social sharing tool button that displays a different image for each of the four different button states.

```
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

The appearance of the panel which contains the individual social sharing icons is controlled with the following CSS class selector:

```
.s7ecatalogsearchviewer .s7socialshare .s7socialsharepanel
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
.s7ecatalogsearchviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```

