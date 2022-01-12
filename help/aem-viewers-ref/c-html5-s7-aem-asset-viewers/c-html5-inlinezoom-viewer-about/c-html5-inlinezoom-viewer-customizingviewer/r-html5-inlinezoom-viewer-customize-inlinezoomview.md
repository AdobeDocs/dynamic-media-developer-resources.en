---
title: Flyout zoom view
description: The main view consists of the static image and the zoomed image shown in the flyout view on top of the static image. It also consists of the tip message shown on top of static image.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 7b4b5cc9-68ad-4e7a-a2d9-3bbced929145
---
# Flyout zoom view{#flyout-zoom-view}

The main view consists of the static image and the zoomed image shown in the flyout view on top of the static image. It also consists of the tip message shown on top of static image.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

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

**CSS properties of the tip message**

The appearance of the tip message is controlled with the following CSS class selector:

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

It is possible to configure font style, size, appearance, and vertical offset through CSS. However, horizontal alignment is managed by the viewer logic. Overriding it through CSS using `left` or `right` properties is not supported.

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

The tip message can be localized. See [Localization of user interface elements](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) for more information.

.

Example - to set up semi-transparent tip message with white Arial® 12-px font, 50 pixels offset from the bottom of the main view, padding, and a rounded border:

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
