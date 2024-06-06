---
title: Embed share
description: Embed share tool consists of a button added to the Social share panel and the modal dialog box that displays when the tool is activated. The position of the button is fully managed by the Social share tool.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: e29a81b8-67f3-4367-b21c-d5902420bc85
---
# Embed share{#embed-share}

Embed share tool consists of a button added to the Social share panel and the modal dialog box that displays when the tool is activated. The position of the button is fully managed by the Social share tool.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

The appearance of the embed share button is controlled with the following CSS class selector:

```
.s7videoviewer .s7embedshare
```

**CSS properties of the embed share tool** 

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Button width. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Button height. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> The image that is displayed for a given button state. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position inside artwork sprite, if CSS sprites are used. </p> <p>See <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>This button supports the `state` attribute selector, which can be used to apply different skins to different button states.

It is possible to remove the button from the Social share panel by setting `display:none` CSS property on its CSS class.

The button tool tip can be localized. See [Localization of user interface elements](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) for more information.

Example - To set up an embed share button that is 28 x 28 pixels, and displays a different image for each of the four different button states:

```
.s7videoviewer .s7embedshare { 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7embedshare[state='up'] { 
background-image:url(images/v2/EmbedShare_dark_up.png); 
} 
.s7videoviewer .s7embedshare[state='over'] { 
background-image:url(images/v2/EmbedShare_dark_over.png); 
} 
.s7videoviewer .s7embedshare[state='down'] { 
background-image:url(images/v2/EmbedShare_dark_down.png); 
} 
.s7videoviewer .s7embedshare[state='disabled'] { 
background-image:url(images/v2/EmbedShare_dark_disabled.png); 
}
```

The background overlay that covers the web page when the dialog box is active, is controlled with the following CSS class selector:

```
.s7videoviewer .s7embeddialog .s7backoverlay
```

**CSS properties of the background overlay** 

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacity </span> </p> </td> 
   <td colname="col2"> <p>Background overlay opacity. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Background overlay color. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up a background overlay to be gray with 70% opacity:

```
.s7videoviewer .s7embeddialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

By default the modal dialog box is displayed centered in the screen on desktop systems and takes the entire web page area on touch devices. In all cases, the positioning and sizing of the dialog box is managed by the component. The dialog box is controlled with the following CSS class selector:

```
.s7videoviewer .s7embeddialog .s7dialog
```

**CSS properties of the dialog box** 

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> Dialog box border radius, in case the dialog box does not take the entire browser. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Dialog box background color. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Should be either unset, or set to 100%, in which case the dialog box takes the entire browser window (this mode is preferred on touch devices). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Should be either unset, or set to 100%, in which case the dialog box takes the entire browser window (this mode is preferred on touch devices). </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up the dialog box to use the entire browser window and have a white background on touch devices:

```
.s7videoviewer .s7touchinput .s7embeddialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

Dialog box header consists of an icon, a title text, and a close button. The header container is controlled with

```
.s7videoviewer .s7embeddialog .s7dialogheader
```

**CSS properties of the dialog box header** 

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p> Inner padding for header content. </p> </td> 
  </tr> 
 </tbody> 
</table>

The icon and the title text are wrapped into an extra container controlled with

```
.s7videoviewer .s7embeddialog .s7dialogheader .s7dialogline
```

**CSS properties of the dialog line** 

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p> Inner padding for the header icon and title </p> </td> 
  </tr> 
 </tbody> 
</table>

Header icon is controlled with the following CSS class selector

```
.s7videoviewer .s7embeddialog .s7dialogheadericon
```

**CSS properties of the dialog box header icon** 

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Icon width. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Icon height. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Icon image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position inside artwork sprite, if CSS sprites are used. </p> <p>See <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Header title is controlled with the following CSS class selector:

```
.s7videoviewer .s7embeddialog .s7dialogheadertext
```

**CSS properties of the dialog box header text** 

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Font weight. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Font height. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Font family. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>Internal text padding. </p> </td> 
  </tr> 
 </tbody> 
</table>

Close button is controlled with the following CSS class selector:

```
.s7videoviewer .s7embeddialog .s7closebutton
```

**CSS properties of the close button ** 

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Vertical button position relative to header container. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p> Horizontal button position relative to header container. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Button width. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Button height. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>Inner padding of button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Button image for each state. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position inside artwork sprite, if CSS sprites are used. </p> <p>See <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>This button supports the `state` attribute selector, which can be used to apply different skins to different button states.

The Close button tool tip and the dialog box title can be localized. See [Localization of user interface elements](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) for more information.

Example - To set up dialog header with padding, 24 x 14 pixels icon, bold 16 point title. And finally, a 28 x 28 pixels close button, positioned two pixels from the top, and two pixels from the right of dialog box container:

```
.s7videoviewer .s7embeddialog .s7dialogheader { 
 padding: 10px; 
} 
.s7videoviewer .s7embeddialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7videoviewer .s7embeddialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgembed_cap.png"); 
    height: 14px; 
    width: 24px; 
} 
.s7videoviewer .s7embeddialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7videoviewer .s7embeddialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7embeddialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7videoviewer .s7embeddialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7videoviewer .s7embeddialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7videoviewer .s7embeddialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

Dialog footer consists of "cancel" button. The footer container is controlled with the following CSS class selector:

```
.s7videoviewer .s7embeddialog .s7dialogfooter
```

**CSS properties of the dialog box footer ** 

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p> Border that you can use to visually separate the footer from the rest of the dialog box. </p> </td> 
  </tr> 
 </tbody> 
</table>

The footer has an inner container which keeps the button. It is controlled with the following CSS class selector:

```
.s7videoviewer .s7embeddialog .s7dialogbuttoncontainer
```

**CSS properties of the dialog box button container** 

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p> Inner padding between the footer and the button. </p> </td> 
  </tr> 
 </tbody> 
</table>

Select All button is controlled with the following CSS class selector:

```
.s7videoviewer .s7embeddialog .s7dialogactionbutton
```

The button is only available on desktop systems.

**CSS properties of the Select All button**

<table id="table_021D0467632F49FEBFDF4CF96D2D67C7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Button width. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Button height. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Button text color for each state. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Button background color for each state. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>The Select All button supports the `state` attribute selector, which can be used to apply different skins to different button states.

Cancel button is controlled with the following CSS class selector:

```
.s7videoviewer .s7embeddialog .s7dialogcancelbutton
```

**CSS properties of the dialog box cancel button** 

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Button width. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Button height. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Button text color for each state. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Button background color for each state. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>The cancel button supports the `state` attribute selector, which can be used to apply different skins to different button states.

In addition, both buttons share common CSS class which can contain CSS settings that are the same for other dialog box buttons:

```
.s7videoviewer .s7embeddialog .s7dialogfooter .s7button
```

**CSS properties of the button** 

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Button font weight. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Button font size. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Button font family. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p> Text height inside the button. Affects vertical alignment. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-shadow </span> </p> </td> 
   <td colname="col2"> <p>Drop shadow. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-right </span> </p> </td> 
   <td colname="col2"> <p>Right button margin. </p> </td> 
  </tr> 
 </tbody> 
</table>

The button tool tips can be localized. See [Localization of user interface elements](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) for more information.

Example - to set up a dialog box footer with a 64 x 34 Cancel button, having text color and background color different for each button state:

```
.s7videoviewer .s7embeddialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7videoviewer .s7embeddialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7videoviewer .s7embeddialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7videoviewer .s7embeddialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7videoviewer .s7embeddialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7videoviewer .s7embeddialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7videoviewer .s7embeddialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7videoviewer .s7embeddialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7videoviewer .s7embeddialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7videoviewer .s7embeddialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7videoviewer .s7embeddialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7videoviewer .s7embeddialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7videoviewer .s7embeddialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

The main dialog area, between the header and the footer, contains scrollable dialog content and scroll panel on the right. In all cases, the component manages the width of this area, it is not possible to set it in CSS. Main dialog area is controlled with the following CSS class selector:

```
.s7videoviewer .s7embeddialog .s7dialogviewarea
```

**CSS properties of the dialog box viewing area ** 

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> The height of the main dialog box area. It should be specified only when the dialog box works in desktop mode. It is not applicable when the dialog box is sized to occupy the entire browser window. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>The background color of the main dialog box area. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>Outer margin. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up a main dialog box area to be 300 pixels height, have a ten pixel margin, and use a white background:

```
.s7videoviewer .s7embeddialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

All form content (like labels and input fields) resides inside a container controlled with

```
.s7videoviewer .s7embeddialog .s7dialogbody
```

If the height of this container appears to be bigger than the main dialog box area, a vertical scroll is enabled automatically by the component.

**CSS properties of the dialog box body ** 

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>Inner padding. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up form content to have ten pixel padding:

```
.s7videoviewer .s7embeddialog .s7dialogbody { 
    padding: 10px; 
}
```

All static labels in the dialog box form are controlled with

```
.s7videoviewer .s7embeddialog .s7dialoglabel
```

This class is not suitable for controlling the label size or position because you can apply it to texts in various places of the form user interface.

**CSS properties of the dialog box label. ** 

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Label font weight. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Label font size. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Label font family. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Label text color. </p> </td> 
  </tr> 
 </tbody> 
</table>

The dialog box labels tool tips can be localized. See [Localization of user interface elements](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) for more information.

Example - to set up all labels to be gray, bold with a nine pixel font:

```
.s7videoviewer .s7embeddialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

The size of the text copy displayed on top of the embed code is controlled with the following CSS class selector:

```
.s7videoviewer .s7embeddialog .s7dialoginputwide
```

**CSS properties of the dialog box input-wide field** 

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Input field width. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>Inner padding. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set text copy to be 430 pixels wide and have a ten pixel padding in the bottom:

```
.s7videoviewer .s7embeddialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

The embed code is wrapped into container and controlled with the following CSS class selector:

```
.s7videoviewer .s7embeddialog .s7dialoginputcontainer
```

**CSS properties of the dialog box input container** 

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>The width of the embed code container. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Border around the embed code container. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>Inner padding. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set a one pixel gray border around embed code text, make it 430 pixels wide, and have a ten pixel padding:

```
.s7videoviewer .s7embeddialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 10px; 
    width: 430px; 
}
```

The actual embed code text is controlled with the following CSS class selector:

```
.s7videoviewer .s7embeddialog .s7dialoginputcontainer
```

**CSS properties of the dialog box input container** 

<table id="table_FEEF66150C69489BB42A2408EBFCE928"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> word-wrap </span> </p> </td> 
   <td colname="col2"> <p>Word wrapping style. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - To set up embedded code so that is use `break-word` word wrapping:

```
.s7videoviewer .s7embeddialog .s7dialogmessage { 
    word-wrap: break-word; 
}
```

Embed size label and drop-down are in the bottom of the dialog box and put into a container controlled with the following CSS class selector:

```
.s7videoviewer .s7embeddialog .s7dialogembedsizepanel
```

**CSS properties of the dialog box embed size panel** 

<table id="table_6BA2769361BA4EC4AB7D250EC9486CB2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>Inner padding. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up an embed size panel to have ten pixels of padding:

```
.s7videoviewer .s7embeddialog .s7dialogembedsizepanel { 
    padding: 10px; 
}
```

The size and alignment of the embed size label is controlled with the following CSS class selector:

```
.s7videoviewer .s7embeddialog .s7dialogembedsizepanel
```

**CSS properties of the dialog box embed size panel** 

<table id="table_8E50C63C9B1349999251CDB5E5AD3D1D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vertical-align </span> </p> </td> 
   <td colname="col2"> <p>Vertical label alignment. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Label width. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set the embed size label to be top-aligned and 80 pixels wide:

```
.s7videoviewer .s7embeddialog .s7dialogembedsizelabel { 
    vertical-align: top; 
    width: 80px; 
}
```

The width of the embed size combo box is controlled with the following CSS class selector:

```
.s7videoviewer .s7embeddialog .s7combobox
```

**CSS properties of the combo box** 

<table id="table_C0FEA0C7353F40039204641BB3F1AE14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Combo box width. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>The combo box supports the `expanded` attribute selector with possible values of `true` and `false`. The `true` value is used when combo box displays one of pre-defined embed sizes, thus should take all available width. The `false` value is used when custom size option is selected in the combo box, so it should shrink to allow space for custom width and height input fields.

Example - To set the embed size combo box to be 300 pixels wide when showing a pre-defined item and 110 pixels wide when showing a custom size:

```
.s7videoviewer .s7embeddialog .s7combobox[expanded="true"] { 
    width: 300px; 
} 
.s7videoviewer .s7embeddialog .s7combobox[expanded="false"] { 
    width: 110px; 
}
```

The height of the combo box text is defined by a special inner element and is controlled with the following CSS class selector:

```
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxtext
```

**CSS properties of the combo box text** 

<table id="table_AB60032BF337433F8455DE20AFBA29AB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Combo box text height. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set embed size combo box text height to 40 pixels:

```
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxtext { 
    height: 40px; 
}
```

The combo box has a "drop down" button on the right and it is controlled with the following CSS class selector:

```
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton
```

**CSS properties of the combo box button** 

<table id="table_70E127FA21264366AD5DBBD7DF40EBAA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Vertical button position inside the combo box. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>Horizontal button position inside the combo box. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Button width. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Button height. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Button image for each state. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position inside artwork sprite, if CSS sprites are used. </p> <p>See <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

This button supports the `state` attribute selector, which can be used to apply different skins to different button states.

Example - to set a "drop down" button to 28 x 28 pixels and have a separate image for each state:

```
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton { 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='up'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
} 
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='over'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='down'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='disabled'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
}
```

The panel with the list of embed sizes displayed when combo box is opened, is controlled with the following CSS class selector:

```
.s7videoviewer .s7embeddialog .s7comboboxdropdown
```

The size and position of the panel is controlled by the component. It is not possible to change it through CSS.

**CSS properties of the combo box drop-down** 

<table id="table_FA7345321C6A4E63B4B78ECF81CE18DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Panel border. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set the combo box panel to have a one pixel gray border:

```
.s7videoviewer .s7embeddialog .s7comboboxdropdown { 
    border: 1px solid #CCCCCC; 
}
```

A single item in a drop-down panel that is controlled with the following CSS class selector:

```
.s7videoviewer .s7embeddialog .s7dropdownitemanchor
```

**CSS properties of the drop-down item anchor** 

<table id="table_FD42FDD56F89463A97FD292FAA04DA5A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Item background. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set the combo box panel item to have a white background:

```
.s7videoviewer .s7embeddialog .s7dropdownitemanchor { 
    background-color: #FFFFFF; 
}
```

A check mark displayed to the left of the selected item inside the combo box panel that is controlled with the following CSS class selector:

```
.s7videoviewer .s7embeddialog .s7checkmark
```

**CSS properties of the check mark box** 

<table id="table_8E01F5461CD04AC18B2C3725A961476A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Icon width. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Icon height. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Item image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position inside artwork sprite, if CSS sprites are used. </p> <p>See <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set the check mark icon to 25 x 25 pixels:

```
.s7videoviewer .s7embeddialog .s7checkmark { 
    background-image: url("images/sdk/cboxchecked.png"); 
    height: 25px; 
    width: 25px; 
}
```

When "Custom Size" option is selected in the embed size combo box, the dialog box displays two extra input fields to the right to allow the user to enter a custom embed size. Those fields are wrapped in a container that is controlled with the following CSS class selector:

```
.s7videoviewer .s7embeddialog .s7dialogcustomsizepanel
```

**CSS properties of the dialog box custom size panel** 

<table id="table_B00829EA550F4E5E8F51B1C6ADACCD34"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p> Distance from the embed size combo box. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set custom size input fields panel to be 20 pixels to the right of the combo box:

```
.s7videoviewer .s7embeddialog .s7dialogcustomsizepanel { 
    left: 20px; 
}
```

Each custom size input field is wrapped in a container that renders a border and sets the margin between the fields. It is controlled with the following CSS class selector:

```
.s7videoviewer .s7embeddialog .s7dialogcustomsize
```

**CSS properties of the dialog box custom size** 

<table id="table_A8A04BE1988641618D0A412B8AEEE1C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Border around the input field. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Input field width. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> Input field margin. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p> Input field padding. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - To set the custom size input fields to have a one pixel gray border, margin, padding, and be 70 pixels wide:

```
.s7videoviewer .s7embeddialog .s7dialogcustomsize { 
    border: 1px solid #CCCCCC; 
    margin-right: 20px; 
    padding-left: 2px; 
    padding-right: 2px; 
    width: 70px; 
}
```

If vertical scrolling is needed, the scroll bar is rendered in the panel near the right edge of the dialog box, which is controlled with the following CSS class selector:

```
.s7videoviewer .s7embeddialog .s7dialogscrollpanel
```

**CSS properties of the dialog box scroll panel** 

<table id="table_BA37E577E0884C919383F84080E2DD28"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Scroll panel width. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up a scroll panel to be 44 pixels wide

```
.s7videoviewer .s7embeddialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

The appearance of scroll bar area is controlled with the following CSS class selector:

```
.s7videoviewer .s7embeddialog .s7scrollbar
```

**CSS properties of the scroll bar** 

<table id="table_066492417FCA43929017993D7326CDB8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Scroll bar width. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> The vertical scroll bar offset from the top of the scroll panel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p> The vertical scroll bar offset from the bottom of the scroll panel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p> The horizontal scroll bar offset from the right edge of the scroll panel. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up a scroll bar that is 28 pixels wide and has an eight pixel margin from the top, right, and bottom of the scroll panel:

```
.s7videoviewer .s7embeddialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

Scroll bar track is the area between the top and bottom scroll buttons. The component automatically sets the position and height of the track. The track is controlled with the following CSS class selector

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolltrack
```

**CSS properties of the scroll bar track** 

<table id="table_19CF5503C1D34ED9998D4F4A6DA7D5D5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Track width. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Track background color. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up a scroll bar track that is 28 pixels wide and has a gray background:

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

The scroll bar thumb moves vertically within a scroll track area. Its vertical position is fully controlled by the component logic. However, thumb height does not dynamically change depending on the amount of content. The thumb height and other aspects can be configured with the following CSS class selector:

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb
```

**CSS properties of the scroll bar thumb** 

<table id="table_90BC468FE138441C9DBAB1EB109F3DB0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Thumb width. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Thumb height. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-top </span> </p> </td> 
   <td colname="col2"> <p>The vertical padding between the top of the track. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-bottom </span> </p> </td> 
   <td colname="col2"> <p> The vertical padding between the bottom of the track. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> The image displayed for a given thumb state. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb supports the `state` attribute selector, which can be used to apply different skins to different thumb states: `up`, `down`, `over`, and `disabled`.

Example - to set up a scroll bar thumb that is 28 x 45 pixels, has a ten pixel margin on the top and bottom, and has different artwork for each state:

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

The appearance of the top and bottom scroll buttons is controlled with the following CSS class selectors:

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton 

```

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton
```

It is not possible to position scroll buttons using CSS top, left, bottom, and right properties. Instead, the viewer logic automatically positions them.

**CSS properties of the top and bottom scroll buttons** 

<table id="table_554BFCFEAF4F43A9AE5F741DC126F833"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Button width. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Button height. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> The image displayed for a given button state. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position inside artwork sprite, if CSS sprites are used. </p> <p>See <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>These buttons support the `state` attribute selector, which can be used to apply different skins to different button states: `up`, `down`, `over`, and `disabled`.

The button tool tips can be localized. See [Localization of user interface elements](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) for more information.

Example - to set up scroll buttons that are 28 x 32 pixels and have different artwork for each state:

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```
