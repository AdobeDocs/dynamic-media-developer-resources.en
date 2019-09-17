---
description: Set indicator is a series of dots rendered at the bottom of the viewer. It shows the current position within the set.
seo-description: Set indicator is a series of dots rendered at the bottom of the viewer. It shows the current position within the set.
seo-title: Set indicator
solution: Experience Manager
title: Set indicator
topic: Dynamic media
uuid: 3f90a216-654f-44a9-947d-592bd5f342d4
---

# Set indicator{#set-indicator}

Set indicator is a series of dots rendered at the bottom of the viewer. It shows the current position within the set.

<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>

**CSS properties of the set indicator**

The appearance of the set indicator container is controlled with the following CSS class selector:

```
.s7carouselviewer .s7setindicator
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

>[!NOTE]
>
>Set indicator supports the mode attribute selector, which you can use to apply different styles for dotted and numeric operation modes. In particular, `mode="numeric"` corresponds to the numeric operation mode; `mode="dotted"` corresponds to the default dot state.

Example - to set up set indicator with a white background:

```
.s7carouselviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

The appearance of an individual set indicator dot is controlled with the CSS class selector. It applies to items both in dotted and numeric operation modes.

`.s7carouselviewer .s7setindicator .s7dot`

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
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Name of font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Size of font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Color of font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vertical-align </span> </p> </td> 
   <td colname="col2"> <p>Vertical alignment of the banner index. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>Text height for the banner index. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Set indicator items support the `state` attribute selector, which can be used to apply different skins to different thumbnail states. In particular, `state="selected"` corresponds to the current element in the set; `state="unselected"` corresponds to the default item state.

Example - to set up set indicator in dotted mode for desktop systems to be positioned 20 pixels from the bottom of the viewer. Unselected dots are black with 50% transparency, 15 x 15 pixels with 7 pixels rounded corners. Selected dots are black with 90% transparency, 18 x 18 pixels with 9 pixels rounded corners. Spacing between dots is 5 pixels.

```
.s7carouselviewer.s7mouseinput .s7setindicator { 
 bottom: 20px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot{ 
 width:15px; 
 height:15px; 
 margin-left:2.5px; 
 margin-right:2.5px; 
 margin-top:2.5px; 
 margin-bottom:2.5px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot[state='selected'] {  
 width:18px; 
 height:18px; 
 background-color: #000000; 
 opacity: 0.9; 
 border-radius:9px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot[state='unselected'] {  
 width:15px; 
 height:15px; 
 background-color: #000000; 
 opacity: 0.5; 
 border-radius:7px; 
}
```

