---
description: The main view consists of the static image, the zoomed image shown in the flyout view, the highlight navigation area displayed over the static image and the tip message shown on top of static image.
seo-description: The main view consists of the static image, the zoomed image shown in the flyout view, the highlight navigation area displayed over the static image and the tip message shown on top of static image.
seo-title: Flyout zoom view
solution: Experience Manager
title: Flyout zoom view
topic: Dynamic media
uuid: 35c60228-3044-442b-a8e2-e13d0bd306a5
---

# Flyout zoom view{#flyout-zoom-view}

The main view consists of the static image, the zoomed image shown in the flyout view, the highlight navigation area displayed over the static image and the tip message shown on top of static image.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

If the dimensions of the image being viewed do not match the dimensions of the flyout zoom view, the image content is centered within the flyout zoom view's rectangle display area.

**CSS properties of the main view**

The appearance of the main view is controlled with the following CSS class selector:

```
.s7flyoutviewer .s7flyoutzoomview
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS property </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> The background color of the main view. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to make the main view transparent:

```
.s7flyoutviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

**CSS properties of the flyout view**

The appearance of the flyout view is controlled with the following CSS class selector:

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom
```

<table id="table_85446C72FD914594B7D108381BBFC673"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS property </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p> The horizontal position of the flyout view, relative to top left corner of main view. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> The vertical position of the flyout view, relative to top left corner of main view. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> The width of the flyout view. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>The height of the flyout view. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>The border of the flyout view. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up a flyout view to 600 x 400 pixels, appearing with 100 pixels offset to the right of the 512 x 288 main view shown in the previous example:

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom { 
 left: 612px; 
 top: 0px; 
 width: 600px; 
 height: 400px;  
}
```

**CSS properties of the highlight in the main view**

The appearance of the highlight in the main view is controlled with the following CSS class selector:

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight
```

It is possible to control background, border, transparency and similar attributes using CSS. However, the size and position of highlight DOM element is managed by the viewer logic. Overriding it through CSS is not supported.

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS property </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> The color of the highlight. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacity </span> </p> </td> 
   <td colname="col2"> <p> Highlight opacity. </p> <p>For Internet Explorer 8, use <span class="codeph"> filter:alpha(opacity-…) ); </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>The border highlight. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up green highlight with 40% transparency and a one pixel red border:

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight { 
 background-color: green; 
 opacity: 0.4;  
 filter: alpha(opacity = 40); 
 border: 1px solid red; 
}
```

**CSS properties of the cursor**

When `highlightmode` parameter is set to `cursor`, highlight are in the main view is replaced with fixed-size cursor artwork, which is controlled with the CSS class selector:

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7cursor
```

It is possible to control the background image and size using CSS.

Applicable CSS properties include:

<table id="table_A86F1E4DE9E84E11AF47373ADC63A459"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS property </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Cursor artwork. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Cursor width. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Cursor height. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Cursor supports the `input` attribute selector, which can be used to apply different cursor artwork and size for different devices. In particular, `input="mouse"` corresponds to the desktop systems and `input="touch"` corresponds to the touch devices.

**CSS properties of the overlay**

When the `overlay` parameter is set to `1`, the area around the highlight frame or the cursor image is controlled with the CSS class selector:

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7overlay
```

<table id="table_A50CA8213C3A4682A081D3D30089574C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS property </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Overlay color. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacity </span> </p> </td> 
   <td colname="col2"> <p>Overlay opacity. </p> </td> 
  </tr> 
 </tbody> 
</table>

**CSS properties of the tip message**

The appearance of the tip message is controlled with the following CSS class selector:

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

It is possible to configure font style, size appearance and vertical offset through CSS. However, horizontal alignment is managed by the viewer logic. Overriding it through CSS using `left` or `right` properties is not supported.

<table id="table_DCF6B69A9D8C4DB7A10C4572F7484799"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS property </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Offset from the bottom of the main view. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Text color. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Font name. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Font size. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>Padding around the message text. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Background fill color of message text. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>Background border radius of message text. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacity </span> </p> </td> 
   <td colname="col2"> <p>Background opacity of message text. </p> <p>For Internet Explorer 8, use <span class="codeph"> filter:alpha(opacity-…) ) </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

The tip message can be localized. See [Localization of user interface elements](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) for more information.

Example - to set up semi-transparent tip message with white Arial 12px font, 50 pixels offset from the bottom of the main view, padding, and a rounded border:

```
.s7flyoutviewer .s7flyoutzoomview .s7tip { 
bottom: 50px; 
color: #ffffff; 
font-family: Arial; 
font-size: 12px; 
padding-bottom: 10px; 
padding-top: 10px; 
padding-left: 12px; 
padding-right: 12px; 
background-color: #000000; 
border-radius: 4px; 
opacity: 0.5; 
filter: alpha(opacity = 50); 
}
```

