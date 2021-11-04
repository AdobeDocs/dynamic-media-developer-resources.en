---
title: Link share
description: Link share tool consists of a button added to the Social share panel and the modal dialog box that displays when the tool is activated. The position of the button is fully managed by the Social share tool.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: a80b47fd-0399-4d0a-8c11-cfa4acc5a713
---
# Link share{#link-share}

Link share tool consists of a button added to the Social share panel and the modal dialog box that displays when the tool is activated. The position of the button is fully managed by the Social share tool.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

The appearance of the link share button is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7linkshare
```

**CSS properties of the link share tool** 

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
   <td colname="col2"> <p> Position inside artwork sprite, if CSS sprites are used. </p> <p>See <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>This button supports the `state` attribute selector, which can be used to apply different skins to different button states.

It is possible to remove the button from the Social share panel by setting `display:none` CSS property on its CSS class.

The button tool tip can be localized. See [Localization of user interface elements](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) for more information.

Example - to set up a link share button that is 28 x 28 pixels, and displays a different image for each of the four different button states:

```
.s7smartcropvideoviewer .s7linkshare { 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7linkshare[state='up'] { 
background-image:url(images/v2/LinkShare_dark_up.png); 
} 
.s7smartcropvideoviewer .s7linkshare[state='over'] { 
background-image:url(images/v2/LinkShare_dark_over.png); 
} 
.s7smartcropvideoviewer .s7linkshare[state='down'] { 
background-image:url(images/v2/LinkShare_dark_down.png); 
} 
.s7smartcropvideoviewer .s7linkshare[state='disabled'] { 
background-image:url(images/v2/LinkShare_dark_disabled.png); 
}
```

The background overlay that covers the web page when the dialog box is active, is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7linkdialog .s7backoverlay
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
.s7smartcropvideoviewer .s7linkdialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

By default the modal dialog box is displayed centered in the screen on desktop systems and takes the entire web page area on touch devices. In all cases, the positioning and sizing of the dialog box is managed by the component. The dialog box is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialog
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
.s7smartcropvideoviewer .s7touchinput .s7linkdialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

Dialog box header consists of an icon, a title text, and a close button. The header container is controlled with

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogheader
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
.s7smartcropvideoviewer .s7linkdialog .s7dialogheader .s7dialogline
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
.s7smartcropvideoviewer .s7linkdialog .s7dialogheadericon
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
   <td colname="col2"> <p> Position inside artwork sprite, if CSS sprites are used. </p> <p>See <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Header title is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogheadertext
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
.s7smartcropvideoviewer .s7linkdialog .s7closebutton
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
   <td colname="col2"> <p> Position inside artwork sprite, if CSS sprites are used. </p> <p>See <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>This button supports the `state` attribute selector, which can be used to apply different skins to different button states.

The Close button tool tip and the dialog box title can be localized. See [Localization of user interface elements](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) for more information.

Example - To set up a dialog box header with padding, 22 x 12 pixels icon, and a bold 16-point title. Finally, a 28 x 28 pixel Close button that is positioned two pixels from the top and two pixels from the right of the dialog box container:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogheader { 
 padding: 10px; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlglink_cap.png"); 
    height: 12px; 
    width: 22px; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7smartcropvideoviewer .s7linkdialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7smartcropvideoviewer .s7linkdialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7smartcropvideoviewer .s7linkdialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

Dialog footer consists of "cancel" button. The footer container is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogfooter
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
.s7smartcropvideoviewer .s7linkdialog .s7dialogbuttoncontainer
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
.s7smartcropvideoviewer .s7linkdialog .s7dialogactionbutton
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
.s7smartcropvideoviewer .s7linkdialog .s7dialogcancelbutton
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
>This button supports the `state` attribute selector, which can be used to apply different skins to different button states.

In addition, both buttons share common CSS class which can contain CSS settings that are the same for other dialog box buttons:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogfooter .s7button
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

The button tool tips can be localized. See [Localization of user interface elements](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) for more information.

Example - to set up a dialog box footer with a 64 x 34 Cancel button, having text color and background color different for each button state:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

The main dialog area (between the header and the footer) contains dialog content. In all cases, the component manages the width of this area—it is not possible to set it in CSS. Main dialog area is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogviewarea
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
.s7smartcropvideoviewer .s7linkdialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

All form content (like labels and input fields) resides inside a container controlled with

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogbody
```

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
.s7smartcropvideoviewer .s7linkdialog .s7dialogbody { 
    padding: 10px; 
}
```

All static labels in the dialog box form are controlled with

```
.s7smartcropvideoviewer .s7linkdialog .s7dialoglabel
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

The dialog box labels can be localized. See [Localization of user interface elements](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) for more information.

Example - to set up all labels to be gray, bold with a nine pixel font:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

The size of the text copy displayed on top of the link is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialoginputwide
```

**CSS properties of the dialog box input-wide field** 

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Text width. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>Inner padding. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set text copy to be 430 pixels wide and have a ten pixel padding in the bottom:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

The share link is wrapped in a container and controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialoginputcontainer
```

**CSS properties of the dialog box input container** 

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Border around the share link container. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>Inner padding. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set a one pixel grey border around embed code text and have nine pixels of padding:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
}
```

The share link itself is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialoglink
```

**CSS properties of the dialog box share link** 

<table id="table_65CF778F5BDA45118208538DCBE203FB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Share link width. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set the share link to be 450 pixels wide:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialoglink { 
    width: 450px; 
}
```
