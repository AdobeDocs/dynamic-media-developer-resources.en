---
title: Email share
description: Email share tool consists of a button added to the Social share panel and the modal dialog box which displays when the tool is activated. The position of the button is fully managed by the Social share tool.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
---
# Email share{#email-share}

Email share tool consists of a button added to the Social share panel and the modal dialog box which displays when the tool is activated. The position of the button is fully managed by the Social share tool.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

The appearance of the email share button is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7emailshare
```

**CSS properties of the email share tool** 

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Width of the button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Height of the button. </p> </td> 
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

This button supports the `state` attribute selector, which can be used to apply different skins to different button states.

It is possible to remove the button from the Social share panel by setting `display:none` CSS property on its CSS class.

The button tool tip can be localized. See [Localization of user interface elements](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) for more information.

Example - to set up an email share button that is 28 x 28 pixels, and that displays a different image for each of the four different button states.

```
.s7smartcropvideoviewer .s7emailshare { 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7emailshare[state='up'] { 
background-image:url(images/v2/EmailShare_dark_up.png); 
} 
.s7smartcropvideoviewer .s7emailshare[state='over'] { 
background-image:url(images/v2/EmailShare_dark_over.png); 
} 
.s7smartcropvideoviewer .s7emailshare[state='down'] { 
background-image:url(images/v2/EmailShare_dark_down.png); 
} 
.s7smartcropvideoviewer .s7emailshare[state='disabled'] { 
background-image:url(images/v2/EmailShare_dark_disabled.png); 
}
```

The background overlay which covers a web page when the dialog box is active, is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7emaildialog .s7backoverlay
```

**CSS properties of the back overlay** 

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacity </span> </p> </td> 
   <td colname="col2"> <p> Background overlay opacity. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Background overlay color. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up background overlay to be gray with 70% opacity:

```
.s7smartcropvideoviewer .s7emaildialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

By default the modal dialog is displayed centered in the screen on desktop systems and takes the whole web page area on touch devices. In all cases, the positioning and sizing of the dialog box is managed by the component. The dialog is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialog
```

**CSS properties of the dialog box** 

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> Dialog box border radius (in case the dialog box does not take the entire browser window); </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Dialog box background color; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Should be either unset, or set to 100%, in which case the dialog takes the whole browser window (this mode is preferred on touch devices); </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Should be either unset, or set to 100%, in which case the dialog takes the whole browser window (this mode is preferred on touch devices). </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up dialog to use entire browser window and have white background on touch devices:

```
.s7smartcropvideoviewer .s7touchinput .s7emaildialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

The dialog box header consists of an icon, a title text, and a Close button. The header container is controlled with the following CSS class selector

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogheader
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
.s7smartcropvideoviewer .s7emaildialog .s7dialogheader .s7dialogline
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
.s7smartcropvideoviewer .s7emaildialog .s7dialogheadericon
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
.s7smartcropvideoviewer .s7emaildialog .s7dialogheadertext
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
.s7smartcropvideoviewer .s7emaildialog .s7closebutton
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

Example - To set up dialog header with padding, 24 x 17 pixels icon, and a bold 16-pt title. And finally, a 28 x 28 pixel Close button, positioned two pixels from the top, and two pixels from the right of dialog container:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogheader { 
 padding: 10px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgemail_cap.png"); 
    height: 17px; 
    width: 24px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

Dialog footer consists of "cancel" and "send email" buttons. The footer container is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogfooter
```

**CSS properties of the dialog box footer ** 

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p> Border which may be used to visually separate the footer from the rest of the dialog box. </p> </td> 
  </tr> 
 </tbody> 
</table>

The footer has an inner container which keeps both buttons. It is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogbuttoncontainer
```

**CSS properties of the dialog box button container** 

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p> Inner padding between the footer and the buttons. </p> </td> 
  </tr> 
 </tbody> 
</table>

Cancel button is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogcancelbutton
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

Send email button is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogactionbutton
```

**CSS properties of the dialog box action button** 

<table id="table_91C75B2470A24DC2AD3973A91FA8B325"> 
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
.s7smartcropvideoviewer .s7emaildialog .s7dialogfooter .s7button
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

Example - To set up a dialog box footer with 64 x 34 Cancel button, and an 82 x 34 Send Email button. And finally, the text color and background color are different for each button state:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

The main dialog area (between the header and the footer) contains scrollable dialog content and scroll panel on the right. In all cases, the component manages the width of this area, it is not possible to set it in CSS. Main dialog area is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogviewarea
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

>[!NOTE]
>
>The main dialog box area supports the optional `state` attribute selector. It is set to `sendsuccess` when the email form is submitted and the dialog box shows a confirmation message. As long as the confirmation message is small, this attribute selector can be used to reduce the dialog box height when such confirmation message is displayed.

Example - to set up the main dialog box area to be 300 pixels height initially and 100 pixels height when the confirmation message is shown, have a ten pixel margin, and use a white background:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogviewarea[state='sendsuccess'] { 
 height:100px; 
}
```

All form content (like labels and input fields) resides inside a container controlled with

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogbody
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
.s7smartcropvideoviewer .s7emaildialog .s7dialogbody { 
    padding: 10px; 
}
```

Dialog box form is filled on line-by-line basis, where each line carries a part of the form content (like a label and a text input field). Single form line is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogbody .s7dialogline
```

**CSS properties of the dialog box line** 

<table id="table_2CCCC71B45B444A8B9CE2894129C9C02"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>Inner line padding. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up a dialog box form to have ten pixel padding for each line:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogbody .s7dialogline { 
    padding: 10px; 
}
```

All static labels in the dialog box form are controlled with

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoglabel
```

This class is not suitable for controlling labels size or position because you can apply it to texts in various places of the form user interface.

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
.s7smartcropvideoviewer .s7emaildialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

All static labels that are displayed to the left of the form input fields are controlled with:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputlabel
```

**CSS properties of the dialog box input label** 

<table id="table_B5CF02837BAA42C7B79B6D9DA20792DF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>The width of the static label. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>The horizontal text alignment. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>Static label margin. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>Static label padding. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up input field labels to be 50 pixels width, right-aligned, have ten pixels of padding, and a ten pixel margin on the right:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputlabel { 
    margin-right: 10px; 
    padding: 10px; 
    text-align: right; 
    width: 50px; 
}
```

Each form input field is wrapped into the container which lets you apply a custom border around the input field. It is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputcontainer
```

**CSS properties of the dialog box input container** 

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Border around the input field container. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>Inner padding. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Input field container supports optional `state` attribute selector. It is set to `verifyerror` when the user makes a mistake in input data format and inline validation fails. This attribute selector can be used to highlight incorrect user input in the form.

Most input fields that spread from the label on the left up to the right edge of the dialog box body (which includes "from" field and "message" field) are controlled with:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputwide
```

**CSS properties of the dialog box input-wide field** 

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Input field width. </p> </td> 
  </tr> 
 </tbody> 
</table>

"To" input field is narrower because it allocates space for "remove email" button on the right. It is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputshort
```

**CSS properties of the dialog box input short field** 

<table id="table_DFA9059209FF4184BD483A529424E97F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Input field width. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - To set up a form to have a one pixel grey border with nine pixels of padding around all input fields. To have the same border in red color for fields which fail validation, to have 250 pixels wide "To" input field, and the rest of the input fields 300 pixels wide:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputcontainer[state="verifyerror"] { 
    border: 1px solid #FF0000; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputshort { 
    width: 250px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputwide { 
    width: 300px; 
}
```

Email message input field is also controlled with:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogmessage
```

This class lets you set specific properties for the underlying `TEXTAREA` element.

**CSS properties of the dialog box message** 

<table id="table_9E9D5A0C3CDB45739615C4C07F8DC046"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Message height. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> word-wrap </span> </p> </td> 
   <td colname="col2"> <p>Word wrapping style. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up an email message to be 50 pixels high and use `break-word` word wrapping:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogmessage { 
    height: 50px; 
    word-wrap: break-word; 
}
```

"Add Another Email Address" button allows a user to add more than one addressee in email form. It is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogaddemailbutton
```

**CSS properties of the dialog box add email address button** 

<table id="table_8829DC0694684E8BA427DFB821F7433D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Button height. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Button text color for each state. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Button image for each state. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>Button image position inside the button area. </p> </td> 
  </tr> 
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
   <td colname="col2"> <p>Text height inside the button. Affects the vertical alignment. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>Horizontal text alignment. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>Inner padding. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>This button supports the `state` attribute selector, which can be used to apply different skins to different button states.

The button tool tip can be localized. See [Localization of user interface elements](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) for more information.

Example - to set up "Add Another Email Address" button to be 25 pixels high, use 12 point bold font with right alignment, and a different text color and image for each state:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogaddemailbutton { 
 text-align:right; 
 font-size:12pt; 
 font-weight:bold; 
 background-position:left center; 
 line-height:25px; 
 padding-left:30px; 
 height:25px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogaddemailbutton[state='up'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogaddemailbutton[state='down'] { 
 color:#000000; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogaddemailbutton[state='over'] { 
 color:#000000; 
 text-decoration:underline; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogaddemailbutton[state='disabled'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
}
```

"Remove" button lets a user remove extra addressees from the email form. It is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogremoveemailbutton
```

**CSS properties of the dialog box remove email button** 

<table id="table_79E4C65741E64859B9C9E9DCCB3D050B"> 
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

The button tool tip can be localized. See [Localization of user interface elements](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) for more information.

Example - to set up a "Remove" button to be 25 x 25 pixels and use a different image for each state:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogremoveemailbutton { 
 width:25px; 
 height:25px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogremoveemailbutton[state='up'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogremoveemailbutton[state='over'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogremoveemailbutton[state='down'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogremoveemailbutton[state='disabled'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
}
```

The content being shared is displayed in the bottom of the dialog box body and includes a thumbnail, title, origin URL, and description. It is wrapped into container controlled with:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogbody .s7dialogcontent
```

**CSS properties of the dialog box content ** 

<table id="table_9C5CBFC2482E4A46BE837573B0B02FE4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Container border. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>Inner padding. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up a bottom container to have a one pixel dotted border and no padding:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogbody .s7dialogcontent { 
    border: 1px dotted #A0A0A0; 
    padding: 0; 
}
```

Thumbnail image is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogthumbnail
```

The `background-image` property is set by the component logic.

**CSS properties of the dialog box thumbnail image** 

<table id="table_4C614FF2CEB149DAB5B7D7BC38CD3CAE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Thumbnail width. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Thumbnail height. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vertical-align </span> </p> </td> 
   <td colname="col2"> <p>Vertical alignment thumbnail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>Inner padding. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up thumbnail to be 90 x 60 pixels, and top-aligned with ten pixels of padding:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogthumbnail { 
    height: 60px; 
    padding: 10px; 
    vertical-align: top; 
    width: 90px; 
}
```

Content title, origin, and description are further grouped into a panel to the right of the content thumbnail. It is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginfopanel
```

**CSS properties of the dialog box information panel** 

<table id="table_EDFA6229D8C3468E989E7EC05F23EF3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Panel width. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up a content information panel to be 300 pixels wide:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginfopanel { 
    width: 300px; 
}
```

Content title is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogtitle
```

**CSS properties of the dialog box title** 

<table id="table_E83C149E66EC474092DF8A180DA9A550"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>Outer margin. </p> </td> 
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

Example - to set up a content title to use bold font and have a ten pixel margin:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogtitle { 
    font-weight: bold; 
    margin: 10px; 
}
```

Content origin is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogorigin
```

**CSS properties of the dialog box content origin ** 

<table id="table_51763B532A9C4AE8AE54B69933A8C0B5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>Outer margin. </p> </td> 
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

Example - to set up content origin to have a ten pixel margin:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogorigin { 
    margin: 10px; 
}
```

Content description is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogdescription
```

**CSS properties of the dialog box content description** 

<table id="table_F0F917ED3D1D4FCE974F48214D287E14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>Outer margin. </p> </td> 
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

Example - to set up a content description to have a ten pixel margin and use a nine point font:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogdescription { 
    font-size: 9pt; 
    margin: 10px; 
}
```

When a user enters incorrect input data and inline validation fails, or when the dialog box must render an error or a confirmation message when the form is submitted, a message is displayed in the top of the dialog box body. It is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogerrormessage
```

**CSS properties of the dialog box error message** 

<table id="table_C114E1004C334D339C25A3438E8E6614"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Error icon. Default is an exclamation mark. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Error icon position inside the message area. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Message text color. </p> </td> 
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
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p> Text height inside the message. Affects vertical alignment. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>Inner padding. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>This message supports the `state` attribute selector with the following possible values: `verifyerror`, `senderror`, and `sendsuccess`. The value `verifyerror` is set when a message is displayed due to an inline input validation failure. The value `senderror` is set when a backend email service reports an error. The `sendsuccess` value is set when email is sent successfully. This way it is possible to style the message differently depending on the dialog box state.

The error message can be localized. See [Localization of user interface elements](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) for more information.

Example - To set up a message to use a ten point bold font, have 25 pixels line height, and 20 pixels padding on the left. Also, use an exclamation mark icon, red text if there is an error, and no icon and green text if there is success:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogerrormessage[state="verifyerror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogerrormessage[state="senderror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogerrormessage[state="sendsuccess"] { 
    background-image: none; 
    color: #00B200; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogerrormessage { 
    background-position: left center; 
    font-size: 10pt; 
    font-weight: bold; 
    line-height: 25px; 
    padding-left: 20px; 
}
```

If vertical scrolling is needed, the scroll bar is rendered in the panel near the right edge of the dialog, which is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogscrollpanel
```

**CSS properties of the dialog box scroll panel** 

<table id="table_A0C3AC7E00544FFBB8E1364F4CDDB371"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Scroll panel width. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up a scroll panel to be 44 pixels wide:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

The appearance of the scroll bar area is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar
```

**CSS properties of the scroll bar** 

<table id="table_2BF74CF43E9B42D79F99A3F5208D7051"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> The scroll bar width. </p> </td> 
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

Example - to set up a scroll bar that is 28 pixels wide, an eight pixel margin from the top, right, and bottom of the scroll panel:

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

Scroll bar track is the area between the top and bottom scroll buttons. The component automatically sets the position and height of the track. The track is controlled with the following CSS class selector:

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolltrack
```

**CSS properties of the scroll track** 

<table id="table_EE990E7A342843619EDD84BAD29C6F2A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>The track width. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>The track background color. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up a scroll bar track that is 28 pixels wide and has a gray background:

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

Scroll bar thumb moves vertically within a scroll track area. Its vertical position is fully controlled by the component logic, however the thumb height does not dynamically change depending on the amount of content. You can configure the thumb height and other aspects with the following CSS class selector:

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollthumb
```

**CSS properties of the scroll bar thumb** 

<table id="table_5A4A283A50044A51881D997885674BDF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>The thumb width. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>The thumb height. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-top </span> </p> </td> 
   <td colname="col2"> <p> The vertical padding between the top of the track. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-bottom </span> </p> </td> 
   <td colname="col2"> <p> The vertical padding between the bottom of the track. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>The image that is displayed for a given thumb state. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position inside artwork sprite, if CSS sprites are used. </p> <p>See <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb supports the `state` attribute selector, which can be used to apply different skins to different thumb states: `up`, `down`, `over`, and `disabled`.

The button tool tips can be localized. See [Localization of user interface elements](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) for more information.

Example - to set up scroll bar thumb that is 28 x 45 pixels, has a ten pixel margin on the top and the bottom, and has different artwork for each state:

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

The appearance of the top and bottom scroll buttons is controlled with the following CSS class selectors:

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton
```

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton  
  
```

**CSS properties of the top and bottom scroll buttons** 

<table id="table_EB853317E08941979B0E141C3C9B2C49"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>The button width. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>The button height. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>The image that is displayed for a given button state. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position inside artwork sprite, if CSS sprites are used. </p> <p>See <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>These buttons support the `state` attribute selector, which can be used to apply different skins to different button states: `up`, `down`, `over`, and `disabled`.

Example - to set up scroll buttons that are 28 x 32 pixels and have different artwork for each state:

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```
