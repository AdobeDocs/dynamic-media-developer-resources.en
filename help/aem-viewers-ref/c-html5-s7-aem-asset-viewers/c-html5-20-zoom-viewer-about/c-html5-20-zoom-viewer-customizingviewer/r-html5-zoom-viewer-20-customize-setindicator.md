---
description: Set indicator is a series of dots rendered on top of swatches when a viewer is used on a touch device. The dots help users to navigate through pages of thumbnails when scroll buttons are not available.
seo-description: Set indicator is a series of dots rendered on top of swatches when a viewer is used on a touch device. The dots help users to navigate through pages of thumbnails when scroll buttons are not available.
seo-title: Set indicator
solution: Experience Manager
title: Set indicator
topic: Dynamic media
uuid: 802916a6-cec5-469b-b54c-dd379925a8c2
index: y
internal: n
snippet: y
---

# Set indicator{#set-indicator}

Set indicator is a series of dots rendered on top of swatches when a viewer is used on a touch device. The dots help users to navigate through pages of thumbnails when scroll buttons are not available.

<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>

**CSS properties of the set indicator**

The appearance of the set indicator container is controlled with the following CSS class selector:

```
.s7zoomviewer .s7setindicator
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
   <td colname="col2"> <p>The background color in hexadecimal format of the set indicator. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up set indicator with a white background:

```
.s7zoomviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

The appearance of an individual set indicator dot is controlled with the CSS class selector:

`.s7zoomviewer .s7setindicator .s7dot`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS property </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Width of the set indicator dot. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Height of the set indicator dot. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p>Left margin in pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p>Top margin in pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-right </span> </p> </td> 
   <td colname="col2"> <p>Right margin in pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-bottom </span> </p> </td> 
   <td colname="col2"> <p>Bottom margin in pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>Border radius in pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Background color in hexadecimal format. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Set indicator dot supports the `state` attribute selector, which can be used to apply different skins to different thumbnail states. In particular, `state="selected"` corresponds to the current page of thumbnails, `state="unselected"` corresponds to the default dot state.

Example - to set up set indicator dot to be 15 x 15 pixels, with two pixels horizontal margin, five pixels top margin, one pixel bottom margin, twelve pixels radius, #D5D3D3 default color, and #939393 active color:

```
.s7zoomviewer .s7setindicator .s7dot { 
 width:15px; 
 height:15px; 
 margin-left:2px; 
 margin-top:5px; 
 margin-right:2px; 
 margin-bottom:1px; 
 border-radius:12px; 
 background-color:#D5D3D3;  
} 
.s7zoomviewer .s7setindicator .s7dot[state="selected"] { 
 background-color:#939393;  
}
```
